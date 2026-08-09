# 07 · Networking

## Interfaces and routes
```bash
ip addr
ip link
ip route
```

## Connectivity
```bash
ping example.com
tracepath example.com
```

## DNS
```bash
getent hosts example.com
nslookup example.com
dig example.com
```

## Sockets
```bash
ss -tuln
ss -lntp
```

## HTTP
```bash
curl -I https://example.com
wget https://example.com/file.zip
```

Troubleshoot in order: link → address → route → DNS → transport → application.
