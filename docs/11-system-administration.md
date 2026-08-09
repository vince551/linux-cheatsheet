# 11 · System Administration

## Identity and host
```bash
hostnamectl
whoami
id
uptime
```

## Hardware and resources
```bash
lscpu
lsusb
lspci
free -h
df -h
lsblk
```

## Services
```bash
systemctl status SERVICE
sudo systemctl restart SERVICE
systemctl is-enabled SERVICE
```

## Firewall concepts
Use your distribution's documented firewall tooling and test changes carefully, especially over remote SSH sessions.
