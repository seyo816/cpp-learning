#### 基础工具安装
```
#基础插件
yum -y install lrzsz screen tree git unzip wget
yum install epel-release -y #先安装epel源
yum install python-pip -y #然后就可以通过yum install python-X来安装python的X库了
pip install --upgrade pip #升级pip到最新版本

#监控工具
yum -y install iotop sysstat htop iftop strace

#编译工具
yum -y install automake cmake  autoconf  libtool

#安装多版本GCC:GCC4.9，GCC5.3，GCC6.2
yum -y install centos-release-scl-rh
#yum install devtoolset-3-gcc devtoolset-3-gcc-c++
#yum install devtoolset-4-gcc devtoolset-4-gcc-c++
yum -y install devtoolset-6-gcc devtoolset-6-gcc-c++
#source /opt/rh/devtoolset-3/enable
#source /opt/rh/devtoolset-4/enable
source /opt/rh/devtoolset-6/enable

# 网络工具
yum -y install bridge-utils
yum install net-tools
yum install iproute
yum install mtr # brew install mtr
yum install traceroute

#安装ip地址显示版本
git clone https://github.com/dzxx36gyy/nali-ipip.git
cd nali-ipip
chmod 777 configure && ./configure && make && make install

```

#### 测试网络命令
```
nali-mtr -r -c 10 -n www.baidu.com

```

#### 测试网络路由
```
#添加bridge
brctl addbr bdocker
ip addr add 172.15.0.1/16 dev bdocker #设置ip 子网掩码
ip link set dev bdocker up #启动
route #多一条路由 172.15.0.0      0.0.0.0         255.255.0.0     U     0      0        0 bdocker
ifconfig # 能看到该路由。

#添加namespace
ip netns add b2
ip netns list

##添加veth1（一对）
ip link add bveth2 type veth peer name bveth2p
ip link show #会看到2条 对应的bveth2@bveth2p bveth2p@bveth2
#插入到bdocker并启动。
brctl addif bdocker bveth2
ip link set bveth2 up
brctl show #bdocker                8000.9298d2cec454       no              bveth2
#插入到另外一个b2 namespace中。
ip link set bveth2p netns b2
ip netns exec b2 ip a
ip netns exec b2 ip link set bveth2p name eth0 #重命名为eth0
ip netns exec b2 ip a
#启动b2下的eth0 并设置ip
ip netns exec b2 ip link set eth0 up
ip netns exec b2 ip addr add 172.15.0.2/16 dev eth0
ip netns exec b2 ifconfig #172.15.0.0/16 dev eth0  proto kernel  scope link  src 172.15.0.2
ip netns exec b2 route #172.15.0.0      0.0.0.0         255.255.0.0     U     0      0        0 eth0
ip netns exec b2 ip route
#b2 下ping 172.15.0.1
ip netns exec b2 ping -c 3 172.15.0.1
#添加路由 来ping 其他的bridge
ip netns exec b2 ip route add default via 172.15.0.1
ip netns exec b2 ip route
#default via 172.15.0.1 dev eth0
#172.15.0.0/16 dev eth0  proto kernel  scope link  src 172.15.0.2
ip netns exec b2 ping -c 3 172.18.0.1

操作第二个ns
ip netns add b3
ip link add bveth3 type veth peer name bveth3p
brctl addif bdocker bveth3
ip link set bveth3 up
ip link set bveth3p netns b3
ip netns exec b3 ip link set bveth3p name eth0
ip netns exec b3 ip link set eth0 up
ip netns exec b3 ip addr add 172.15.0.3/16 dev eth0
ip netns exec b3 ip route add default via 172.15.0.1

#集成测试
ip netns exec b3 ping -c 3 172.15.0.1
ip netns exec b3 ping -c 3 172.18.0.1
ping 172.15.0.3
ping 172.15.0.2
ping 172.15.0.1

ip netns exec b2 ping -c 3 172.15.0.3
ip netns exec b3 ping -c 3 172.15.0.2
```
