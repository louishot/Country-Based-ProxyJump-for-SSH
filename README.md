cat ~/.ssh/config 

```
Host proxy-server1
    HostName 192.168.100.221

Match Exec "curl -s https://ipinfo.io/%h | grep '"country": "CN"'"
    ProxyJump proxy-server1
```
