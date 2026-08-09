# 08 · Bash & Shell

```bash
NAME="Vince"
echo "$NAME"
TODAY=$(date)
echo "$TODAY"
```

## Pipes and redirection
```bash
ps aux | grep nginx
echo 'hello' > file.txt
echo 'world' >> file.txt
command 2> errors.log
command > output.log 2>&1
```

## Safe script starter
```bash
#!/usr/bin/env bash
set -euo pipefail

echo "User: $USER"
echo "Directory: $PWD"
```

Run with:
```bash
chmod +x script.sh
./script.sh
```
