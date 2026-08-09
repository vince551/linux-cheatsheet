# 12 · Logs & Troubleshooting

## systemd logs
```bash
journalctl
journalctl -n 50
journalctl -f
journalctl -u SERVICE
```

## Kernel messages
```bash
dmesg
```

## Troubleshooting loop
```text
Observe → Reproduce → Isolate → Check logs → Test one change → Verify → Document
```

Always record what changed before a failure, reproduce it where possible, and change one variable at a time.
