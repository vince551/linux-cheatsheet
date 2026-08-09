# 04 · Processes & Services

## Processes
```bash
ps aux
top
htop
pgrep firefox
```

## Signals
```bash
kill PID
kill -TERM PID
kill -9 PID
```
Use graceful termination before `SIGKILL`.

## systemd
```bash
systemctl status service
sudo systemctl start service
sudo systemctl stop service
sudo systemctl restart service
sudo systemctl enable service
journalctl -u service
```
