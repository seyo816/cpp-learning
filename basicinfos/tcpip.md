[ TCP、UDP、IP 协议分析 ](http://blog.chinaunix.net/uid-26833883-id-3627644.html)


输入PING ping www.baidu.com

WIRESHAR过滤规则
```
icmp

ip.src eq 192.168.1.107
ip.dst eq 192.168.1.107
ip.addr eq 58.217.200.113
tcp.port == 22222
ip.dst eq 127.0.0.1

```
