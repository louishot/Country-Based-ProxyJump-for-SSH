cat ~/.ssh/config 

```
Host proxy-server1
    HostName 192.168.100.221
    IdentityFile ~/.ssh/key2

Exec "curl -s https://ipinfo.io/%h | jq .country | grep CN"
    ProxyJump proxy-server1
    
    
```
