# requests加上ss代理
```
import ujson as json
import requests
import socks
import socket


# 代理
socks.set_default_proxy(socks.SOCKS5, "localhost", 1080)
socket.socket = socks.socksocket

```
