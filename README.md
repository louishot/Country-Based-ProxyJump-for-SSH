cat ~/.ssh/config 

```
Host proxy-server1
    HostName 192.168.100.221

Match Exec "curl -s https://ipinfo.io/%h | grep '"country": "CN"'"
    ProxyJump proxy-server1
    
Host proxy-server2
    HostName 192.168.101.221

Match Exec "curl -s https://ipinfo.io/%h | grep '"city": "Los Angeles"'"
    ProxyJump proxy-server2
    
Match Exec "curl -s https://ipinfo.io/%h | grep '"org": "AS16509'"
    ProxyJump proxy-server2
    
```
