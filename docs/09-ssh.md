# 09 · SSH & Remote Administration

## Connect
```bash
ssh user@server
```

## Generate a key
```bash
ssh-keygen -t ed25519
```

## Copy files
```bash
scp file.txt user@server:/path/
```

## Inspect configuration
```bash
ssh -G user@server
```

Security basics: protect private keys, prefer key authentication, update systems, minimize exposed services and review authentication logs. Only access systems you are authorized to administer.
