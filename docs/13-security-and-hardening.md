# 13 · Security & Hardening

## Baseline
- Update packages.
- Remove unnecessary services.
- Apply least privilege.
- Use strong authentication.
- Protect SSH private keys.
- Configure a firewall where appropriate.
- Monitor logs.
- Back up important data.

## Inspect
```bash
ss -lntup
ls -la
whoami
id
sudo -l
journalctl -p warning..alert
```

Security work should be performed on systems you own or have explicit authorization to assess. Prefer isolated labs for experimentation.
