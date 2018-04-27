# arp-devops
* ARP (Address Resolve Protocol) [rfc826](https://tools.ietf.org/html/rfc826)

* 清理ARP缓存

```
情景：使用keepalived的时候主机挂了，备机显示绑定了VIP。但是此时实际还是不能访问。其实就是网关的arp缓存没有刷新。
命令：arping -I 网卡名称 -c 5 -s IP GATEWAY
查看 IP GATEWAY 命令：netstat -rn
```