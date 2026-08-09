# 03 · Users & Permissions

## Inspect identity
```bash
whoami
id
who
w
```

## Permissions
```bash
ls -l
chmod 644 file.txt
chmod 755 script.sh
chmod +x script.sh
```

`r=4`, `w=2`, `x=1`.

## Ownership
```bash
sudo chown user:user file.txt
sudo chgrp group file.txt
```

## User management
```bash
sudo adduser learner
sudo usermod -aG sudo learner
passwd
```

Follow least privilege. Avoid unnecessary root access.
