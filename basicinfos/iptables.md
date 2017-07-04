

#### Iptables基础配置
```
#安装
yum install iptables-services
systemctl  restart iptables
service iptables save
iptables-save #临时保存
iptables-save > /etc/sysconfig/iptables


iptables -t filter -L -n
iptables -t nat -L
iptables -L -n --line-number
iptables -L -n -v #带IP 带流量

iptables -A INPUT -p tcp -m state --state NEW --dport 8000 -j ACCEPT
iptables -I INPUT 4 -p tcp --dport 8000 -j ACCEPT
iptables -I INPUT 5 -p tcp --dport 8888 -j ACCEPT
iptables -I INPUT 6 -p tcp --dport 8889 -j ACCEPT
iptables -D INPUT 4

iptables -D INPUT 2
iptables -I INPUT 2 -p icmp -j ACCEPT

局域网：-A INPUT -s 192.168.0.0/255.255.0.0 -m comment --comment "local" -j ACCEPT

```

#### traceroute
```
你要好好理解一下 ICMP traceroute的原理就知道了

使用ICMP Echo Request, Echo Reply and TTL-expired.

源发出 ICMP Equest，第一个request的TTL为1，第二个request的TTL为2，以后依此递增直至第30个；
中间的router送回ICMP TTL-expired ( ICMP type 11) 通知source，（packet同时因TTL超时而被drop)，
由此source知晓一路上经过的每一个router；最后的destination 送回ICMP Echo Reply（最后一跳不会再
回ICMP TTL-expired）。

所以中间任何一个router上如果封了ICMP Echo Request, traceroute就不能工作；如果封了type 11
 (TTL-expired), 中间的router全看不到，但能看到packet 到达了最后的destination；
如果封了ICMP Echo Reply，中间的全能看到，最后的destination看不到。

多重路由，导致每次tracetoute出去路径不一样。
计算时长，包括回来的，回来的路径不一定是出去的route。
linux下默认是发udp包。
traceroute -T -n www.baidu.com
traceroute -I www.baidu.com

```

#### 端口转发
* 转发功能

```
cat /porc/sys/net/ipv4/ip_forward #开是否是1
echo 1 > /porc/sys/net/ipv4/ip_forward #这是个暂时的做法，重启后就会失效，好的做法是：
#sed -i 's#net.ipv4.ip_forward = 0#net.ipv4.ip_forward = 1#g' /etc/sysctl.conf
#sysctl -p

```

##### IPTABLES（DNAT+SNAT）

* 配置防火墙

```
#curl -I http://122.112.242.2:8000 默认弹性IP 192.168.1.7。所以下面要配置的是内网IP(只有一个内网IP可以不指定-d 122.112.242.2 )。如果ifconfig能直接看到外网IP则设置外网IP.filters中可以不用开放8888端口。
#curl -I http://122.112.242.2:8888
iptables -t nat -F
iptables -t nat -A PREROUTING  -p tcp --dport 8888 -j DNAT --to-destination 192.168.1.7:8000 #-d 122.112.242.2
#因为是内网IP，所以下面这个可以不用设置。
iptables -t nat -A POSTROUTING -d 192.168.1.7/32 -p tcp -m tcp --sport 8000 -j SNAT --to-source 192.168.1.7
```

```
#外部转发 配置不通过
#hwcloud
iptables -t nat -F
iptables -t nat -A PREROUTING  -p tcp --dport 8888 -j DNAT --to-destination 59.110.234.196:8000
iptables -t nat -A POSTROUTING -d 59.110.234.196 -p tcp -m tcp --dport 8000 -j SNAT --to-source 192.168.1.7

#nioayun 直接外网网卡 ok
#curl -I http://118.192.148.57:8888
iptables -t nat -A PREROUTING -d 118.192.148.57 -p tcp --dport 8888 -j DNAT --to-destination 59.110.234.196:8000
iptables -t nat -A POSTROUTING -d 59.110.234.196 -p tcp --dport 8000 -j SNAT --to 118.192.148.57

```

```
#docker 防火墙解析

iptables -t nat -A POSTROUTING -s 192.168.0.0/24 -o eth0 -j MASQUERADE
重点在那个『 MASQUERADE 』！这个设定值就是『IP伪装成为封包出去(-o)的那块装置上的IP

```

##### Haproxy
```

yum -y install haproxy
cat > /etc/haproxy/haproxy.cfg <<EOF
global
        ulimit-n  51200
defaults
        log global
        mode    tcp
        option  dontlognull
        timeout connect 5000ms  #连接超时
        timeout client 30000ms  #客户端超时
        timeout server 10000ms  #服务器超时

frontend ss-in
        bind *:8888
        default_backend ss-out

backend ss-out
        server server1 59.110.234.196:8000 maxconn 20480
EOF
pkill haproxy && haproxy -f /etc/haproxy/haproxy.cfg &

```
##### LVS
* [lvs说明](http://www.cnblogs.com/MacoLee/p/5856858.html)

```
#curl -I http://122.112.242.2:8889
yum -y install ipvsadm
ipvsadm-save
ipvsadm-save > /etc/sysconfig/ipvsadm
systemctl restart ipvsadm

ipvsadm -L
ipvsadm -L -n

lsmod |grep ip_vs

```
* LVS+NAT

```
ipvsadm -C
#添加VIP+PORT 负载策略：轮询
ipvsadm -A -t 192.168.1.7:8889 -s rr
#VIP+PORT ----> RIP+PORT 负载模式NAT
ipvsadm -a -t 192.168.1.7:8889  -r 59.110.234.196:8000 -m

#内网配置ok
ipvsadm -C
ipvsadm -A -t 192.168.1.7:8889 -s rr
ipvsadm -a -t 192.168.1.7:8889  -r 192.168.1.7:8000 -m
#添加多个就是集群
ipvsadm -a -t 192.168.1.7:8889  -r 192.168.1.7:8001 -m


```

* LVS+DR

```

```

[9个常用iptables配置实例](http://www.cnblogs.com/bangerlee/archive/2013/02/27/2935422.html)


IPTABLES LVS HAPROXY TPROXY NGINX
HATOP SQUID KEEPALIVE

sysctl -a | grep ip_forward


yum install haproxy

cat > /etc/haproxy/haproxy.cfg <<EOF
global
        daemon
        nbproc 10
        pidfile /var/run/haproxy.pid
defaults
        mode tcp               #默认的模式mode { tcp|http|health }，tcp是4层，http是7层，health只会返回OK
        retries 2               #两次连接失败就认为是服务器不可用，也可以通过后面设置
        option abortonclose     #当服务器负载很高的时候，自动结束掉当前队列处理比较久的链接
        maxconn 65535            #默认的最大连接数
        timeout connect 5000ms  #连接超时
        timeout client 30000ms  #客户端超时
        timeout server 10000ms  #服务器超时
        log 127.0.0.1 local0 err #[err warning info debug]
listen test1
        bind 0.0.0.0:8001
        mode tcp
        server s1 59.110.234.196:8000
EOF

cat > /etc/haproxy/haproxy.cfg <<EOF
global
        ulimit-n  51200
defaults
        log global
        mode    tcp
        option  dontlognull
        timeout connect 5000ms  #连接超时
        timeout client 30000ms  #客户端超时
        timeout server 10000ms  #服务器超时

frontend ss-in
        bind *:8001
        default_backend ss-out

backend ss-out
        server server1 59.110.234.196:8000 maxconn 20480
EOF




curl -I 59.110.234.196:8000
curl -I 118.192.148.57:8001
