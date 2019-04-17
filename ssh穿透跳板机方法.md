# 添加配置进入~/.ssh/config
```
Host tiaoban
     HostName 192.168.xxx.xxx
     Port 22
     User work

Host node1
     HostName 106.14.xxx.xxx
     Port 22
     User root
     ProxyCommand ssh work@tiaoban -W %h:%p

```
