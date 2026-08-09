<div align="center">

# 🐧 LINUX MASTERY

### The Linux Learning Hub & Field Manual

**Learn • Practice • Build • Administer • Secure**

<br>

[![Linux](https://img.shields.io/badge/Linux-000000?style=for-the-badge&logo=linux&logoColor=white)](https://www.linux.org/)
[![Bash](https://img.shields.io/badge/Bash-121011?style=for-the-badge&logo=gnubash&logoColor=white)](https://www.gnu.org/software/bash/)
[![Debian](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white)](https://www.debian.org/)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)](https://ubuntu.com/)
[![Kali](https://img.shields.io/badge/Kali-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)](https://www.kali.org/)
[![Termux](https://img.shields.io/badge/Termux-000000?style=for-the-badge&logo=android&logoColor=white)](https://termux.dev/)

<br>

> **A practical, colorful and structured Linux reference — from your first `pwd` to system administration, networking, development and security labs.**

</div>

---

## 🌟 What is this?

**Linux Mastery** is designed as a complete learning hub rather than a single cheat sheet. It combines quick-reference commands, explanations, visual guides, practice exercises, troubleshooting notes and security-aware workflows in one place.

Use it in three ways:

| Mode | Use it for |
|---|---|
| ⚡ **Quick Reference** | Find a command in seconds |
| 🎓 **Learning Path** | Learn Linux progressively from beginner to advanced |
| 🧪 **Practice Lab** | Turn commands into hands-on skills |

---

## 🖼️ Visual Learning Gallery

> The repository is designed to pair the written lessons with visual references. Place the four supplied reference images in `assets/` using the filenames below.

<div align="center">

| 🐧 Command Map | 🧠 How Linux Works |
|---|---|
| ![Linux commands](assets/linux-commands.jpg) | ![How Linux works](assets/how-linux-works.jpg) |

| 🛡️ Kali Tools | 🌈 Linux Beginner Map |
|---|---|
| ![Kali Linux tools](assets/kali-tools.jpg) | ![Linux learning](assets/linux-learning.jpg) |

</div>

---

# 🧭 Start Here

### If you are completely new to Linux

Follow this order:

```text
01  Terminal & Linux concepts
        ↓
02  Filesystem & navigation
        ↓
03  Files & directories
        ↓
04  Users, groups & permissions
        ↓
05  Processes & services
        ↓
06  Packages & software
        ↓
07  Networking
        ↓
08  Bash & automation
        ↓
09  Storage & system administration
        ↓
10  Git & development
        ↓
11  Logs, troubleshooting & hardening
        ↓
12  Kali Linux & authorized security labs
        ↓
13  Termux & mobile Linux
```

### 🎯 The goal

Don't memorize hundreds of commands.

Learn the pattern:

```text
COMMAND → OPTIONS → TARGET → RESULT
```

Then learn **why** the command works, **when** to use it, and **what could go wrong**.

---

# 📚 Learning Hub

## 🟢 Level 1 — Linux Fundamentals

- [01 · Linux fundamentals](docs/01-linux-fundamentals.md)
- [02 · Files & directories](docs/02-files-and-directories.md)
- [03 · Users & permissions](docs/03-users-and-permissions.md)

## 🔵 Level 2 — System Skills

- [04 · Processes & services](docs/04-processes-and-services.md)
- [05 · Package management](docs/05-package-management.md)
- [06 · Storage & filesystems](docs/06-storage-and-filesystems.md)

## 🟣 Level 3 — Networking & Shell

- [07 · Networking](docs/07-networking.md)
- [08 · Bash & shell](docs/08-bash-and-shell.md)
- [09 · SSH & remote administration](docs/09-ssh.md)

## 🟠 Level 4 — Development & Administration

- [10 · Git & development](docs/10-git-and-development.md)
- [11 · System administration](docs/11-system-administration.md)
- [12 · Logs & troubleshooting](docs/12-logs-and-troubleshooting.md)

## 🔴 Level 5 — Security Learning

- [13 · Linux security & hardening](docs/13-security-and-hardening.md)
- [14 · Kali Linux learning path](docs/14-kali-linux.md)
- [15 · Termux & mobile Linux](docs/15-termux.md)

---

# ⚡ 60-Second Linux Cheat Sheet

```bash
# Where am I?
pwd

# What's here?
ls -lah

# Move around
cd /path/to/folder
cd ..
cd ~

# Create
mkdir project
touch notes.txt

# Read
cat notes.txt
less notes.txt

# Copy / move
cp notes.txt backup.txt
mv backup.txt docs/

# Search
find . -name "*.txt"
grep -R "keyword" .

# System
uname -a
cat /etc/os-release
whoami
id
uptime

# Resources
df -h
free -h
ps aux

# Network
ip a
ip route
ss -tuln
ping example.com
curl -I https://example.com

# Debian / Ubuntu / Kali
sudo apt update
sudo apt upgrade
sudo apt install <package>
```

---

# 📁 Filesystem Essentials

Linux treats almost everything as a file or a file-like resource.

```text
/
├── bin/      Essential commands
├── boot/     Boot files
├── dev/      Devices
├── etc/      Configuration
├── home/     User directories
├── lib/      Libraries
├── media/    Removable media
├── mnt/      Temporary mounts
├── opt/      Optional software
├── proc/     Process/kernel information
├── root/     Root user's home
├── run/      Runtime data
├── sbin/     System binaries
├── srv/      Service data
├── sys/      Kernel/device information
├── tmp/      Temporary files
├── usr/      User applications and data
└── var/      Logs, caches and variable data
```

### Navigation

```bash
pwd
ls
ls -lah
cd /etc
cd ..
cd ~
cd -
```

### Create and manage files

```bash
mkdir project
mkdir -p project/src/components
touch app.log
cp app.log app.backup.log
mv app.log logs/
rm app.backup.log
```

> ⚠️ `rm` permanently removes files in normal command-line workflows. Check the target before using recursive deletion.

---

# 👤 Users, Groups & Permissions

Linux permissions are built around **owner**, **group**, and **others**.

```text
-rwxr-xr--
 ||| ||| |||
 ||| ||| +++ → others
 ||| +++     → group
 +++         → owner
```

### Inspect permissions

```bash
ls -l
stat file.txt
```

### Change permissions

```bash
chmod 644 file.txt
chmod 755 script.sh
chmod +x script.sh
```

### Ownership

```bash
sudo chown user:user file.txt
sudo chgrp developers file.txt
```

### User management

```bash
whoami
id
who
w
passwd
```

On Debian-based systems:

```bash
sudo adduser newuser
sudo usermod -aG sudo newuser
```

### Permission principle

> **Use the least privilege necessary.** Avoid running everything as `root`.

---

# ⚙️ Processes & Services

A process is a running instance of a program.

### Inspect processes

```bash
ps aux
ps -ef
top
htop
pgrep firefox
```

### Stop a process

```bash
kill <PID>
kill -TERM <PID>
kill -9 <PID>
```

Use normal termination first; `SIGKILL` should be a last resort.

### systemd

```bash
systemctl status <service>
sudo systemctl start <service>
sudo systemctl stop <service>
sudo systemctl restart <service>
sudo systemctl enable <service>
systemctl is-enabled <service>
```

---

# 📦 Package Management

| Distribution family | Main tool | Example |
|---|---|---|
| Debian / Ubuntu / Kali | `apt` | `sudo apt install git` |
| Fedora / RHEL | `dnf` | `sudo dnf install git` |
| Arch | `pacman` | `sudo pacman -S git` |
| Alpine | `apk` | `sudo apk add git` |

### Debian-based workflow

```bash
sudo apt update
sudo apt upgrade
apt search <package>
sudo apt install <package>
sudo apt remove <package>
apt show <package>
```

> Keep repositories and packages trustworthy. Don't paste random installation commands from untrusted sources into a privileged shell.

---

# 🌐 Networking

### Interfaces and addresses

```bash
ip addr
ip link
ip route
```

### Connectivity

```bash
ping example.com
tracepath example.com
```

### Listening sockets

```bash
ss -tuln
ss -lntp
```

### DNS

```bash
getent hosts example.com
nslookup example.com
dig example.com
```

### HTTP

```bash
curl https://example.com
curl -I https://example.com
wget https://example.com/file.zip
```

### Network troubleshooting model

```text
LINK
 ↓
IP ADDRESS
 ↓
ROUTE
 ↓
DNS
 ↓
TCP/UDP
 ↓
APPLICATION
```

When a network problem occurs, troubleshoot from the bottom up.

---

# 🐚 Bash & Shell

### Pipes

```bash
ls -lah | less
ps aux | grep nginx
journalctl | grep -i error
```

### Redirection

```bash
echo "hello" > file.txt
echo "another line" >> file.txt
command 2> errors.log
command > output.log 2>&1
```

### Variables

```bash
NAME="Vince"
echo "$NAME"
```

### Command substitution

```bash
TODAY=$(date)
echo "$TODAY"
```

### Script template

```bash
#!/usr/bin/env bash
set -euo pipefail

echo "Linux Mastery"
echo "User: $USER"
echo "Directory: $PWD"
```

Run it:

```bash
chmod +x script.sh
./script.sh
```

---

# ⌨️ Terminal Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl + C` | Stop current command |
| `Ctrl + Z` | Suspend current process |
| `Ctrl + D` | Exit / EOF |
| `Ctrl + L` | Clear terminal view |
| `Ctrl + R` | Search command history |
| `Tab` | Autocomplete |
| `↑ / ↓` | Command history |
| `!!` | Repeat previous command |
| `history` | Show history |

---

# 🔎 Search & Locate

```bash
find . -name "file.txt"
find . -type f -name "*.log"
find . -type d -name "node_modules"

grep "error" app.log
grep -R "TODO" .
grep -n "listen" server.js

command -v python
which git
whereis bash
```

For large searches, combine tools:

```bash
find . -type f -name "*.js" -print0 | xargs -0 grep -n "fetch"
```

---

# 🗜️ Archives & Compression

### tar

```bash
tar -cvf archive.tar folder/
tar -xvf archive.tar

tar -czvf archive.tar.gz folder/
tar -xzvf archive.tar.gz
```

### zip

```bash
zip -r archive.zip folder/
unzip archive.zip
```

### gzip

```bash
gzip file.txt
gunzip file.txt.gz
```

---

# 📝 Text Processing

```bash
cat file.txt
head file.txt
tail file.txt
tail -f app.log
less file.txt
```

### grep

```bash
grep "word" file.txt
grep -i "word" file.txt
grep -n "word" file.txt
```

### sort / uniq / wc

```bash
sort names.txt
sort names.txt | uniq
wc -l names.txt
```

### awk / sed

```bash
awk '{print $1}' file.txt
sed 's/old/new/g' file.txt
```

---

# 💾 Storage & Filesystems

```bash
df -h
du -sh .
du -sh *
lsblk
blkid
mount
findmnt
```

### Important distinction

```text
lsblk → physical/virtual block devices
mount → mounted filesystems
df   → filesystem capacity
 du  → directory/file usage
```

> ⚠️ Disk commands such as `dd`, `mkfs`, partitioning tools and raw-device operations can destroy data. Use them only when you fully understand the target device.

---

# 🔐 SSH & Remote Administration

### Connect

```bash
ssh user@server
```

### Generate a modern key

```bash
ssh-keygen -t ed25519
```

### Inspect the public key

```bash
cat ~/.ssh/id_ed25519.pub
```

### Copy files

```bash
scp file.txt user@server:/path/
```

### Security basics

- Prefer key authentication.
- Protect private keys.
- Disable unnecessary services.
- Keep the operating system updated.
- Use a firewall where appropriate.
- Review authentication logs.

---

# 🧑‍💻 Git & Development

```bash
git clone <repository>
cd <repository>
git status
git add .
git commit -m "message"
git pull
git push
```

### Branches

```bash
git branch
git switch -c feature/name
git switch main
git merge feature/name
```

### Inspect history

```bash
git log --oneline --graph --decorate
```

---

# 🛠️ System Information

```bash
uname -a
cat /etc/os-release
hostnamectl
hostname
whoami
id
uptime
free -h
df -h
lsblk
```

### Hardware

```bash
lscpu
lsusb
lspci
```

Availability varies by distribution and installation.

---

# 📜 Logs & Troubleshooting

### systemd logs

```bash
journalctl
journalctl -n 50
journalctl -f
journalctl -u <service>
```

### Kernel messages

```bash
dmesg
```

### Troubleshooting loop

```text
OBSERVE
  ↓
REPRODUCE
  ↓
ISOLATE
  ↓
CHECK LOGS
  ↓
TEST ONE CHANGE
  ↓
VERIFY
  ↓
DOCUMENT
```

### Useful questions

1. What changed?
2. Can I reproduce it?
3. Is the problem local or remote?
4. What do the logs say?
5. Is a service running?
6. Is there enough CPU, memory or disk space?
7. Are permissions correct?
8. Did networking/DNS change?

---

# 🛡️ Linux Security & Hardening

Security starts with good system administration.

### Core checklist

```text
[ ] Keep packages updated
[ ] Use strong authentication
[ ] Prefer SSH keys
[ ] Minimize exposed services
[ ] Apply least privilege
[ ] Configure a firewall where appropriate
[ ] Monitor logs
[ ] Back up important data
[ ] Protect secrets and private keys
[ ] Remove unnecessary software
[ ] Test changes in a safe environment
```

### Inspect listening services

```bash
ss -lntup
```

### Check permissions

```bash
ls -la
```

### Review system identity

```bash
whoami
id
sudo -l
```

Use security tooling only against systems you own or have explicit permission to test.

---

# 🐉 Kali Linux Learning Path

Kali Linux is a Debian-based security-focused distribution. Learn the underlying Linux concepts before relying on specialized tools.

```text
Linux Fundamentals
       ↓
Networking
       ↓
Web Fundamentals
       ↓
Security Concepts
       ↓
Authorized Labs
       ↓
Kali Tooling
       ↓
Defensive Analysis
```

### Common tool categories

| Area | Examples |
|---|---|
| 🔎 Reconnaissance | Nmap |
| 🧪 Web testing | Burp Suite |
| 📡 Packet analysis | Wireshark |
| 🧰 Frameworks | Metasploit |
| 🔬 Forensics | Autopsy / forensic utilities |
| 🛡️ Defense | Wireshark, logs, system tooling |

The purpose of this section is **authorized security education**. Use labs, CTFs and systems you are permitted to assess.

---

# 📱 Termux & Mobile Linux

Termux provides a terminal environment on Android.

```bash
pkg update
pkg upgrade
pkg install git
pkg install python
termux-setup-storage
```

### Understand the difference

```text
Android
  ↓
Termux application
  ↓
Termux userland
  ↓
Optional proot/container-like Linux environments
```

A Termux environment is not identical to a normal desktop Linux installation. Android permissions, CPU architecture and kernel restrictions matter.

---

# 🧪 Practice Labs

## 🟢 Beginner Lab — File Manager

Goal: create and organize a project.

```bash
mkdir -p ~/linux-lab/{docs,scripts,backup}
touch ~/linux-lab/docs/notes.txt
echo "My first Linux lab" > ~/linux-lab/docs/notes.txt
cat ~/linux-lab/docs/notes.txt
```

Tasks:

- Create three files.
- Copy one into `backup/`.
- Move one into `docs/`.
- Find all `.txt` files.
- Remove a test file.

## 🔵 Intermediate Lab — System Investigator

Collect information without changing the system:

```bash
uname -a
cat /etc/os-release
whoami
id
uptime
free -h
df -h
ip a
ip route
ss -tuln
```

Write down what each command tells you.

## 🟣 Shell Lab — Log Analyzer

```bash
grep -i "error" app.log | sort | uniq -c | sort -nr
```

Goal: identify repeated errors and explain the pipeline.

## 🔴 Security Lab — Authorized Environment

Use a dedicated VM, CTF or lab environment. Practice identifying services, reading logs and applying hardening changes. Never scan or attack systems without authorization.

---

# 🎯 Command Learning Method

For every new command, answer five questions:

```text
1. WHAT does it do?
2. WHY would I use it?
3. WHAT are the important options?
4. WHAT could go wrong?
5. HOW can I practice safely?
```

Example:

```bash
chmod 755 script.sh
```

**What:** changes permission bits.

**Why:** commonly used to make a script executable.

**Risk:** recursive or broad permission changes can weaken security.

**Practice:** use a disposable lab directory.

---

# ⚠️ Dangerous Commands

Treat these with extra care:

```bash
rm -rf
dd
mkfs
fdisk
parted
chmod -R
chown -R
```

Never run a destructive command simply because someone posted it online.

Before using a privileged or destructive command:

```text
READ → UNDERSTAND → VERIFY TARGET → BACK UP → EXECUTE
```

---

# 🧠 Linux Concepts You Should Understand

A strong Linux user should eventually understand:

- Kernel vs user space
- Processes and PIDs
- File descriptors
- Permissions and ownership
- Environment variables
- PATH
- Pipes and redirection
- Signals
- Services and systemd
- Filesystems and mounts
- TCP/IP basics
- DNS
- SSH
- Package managers
- Logs
- Shell scripting
- Git
- Backups
- Security principles

---

# 🌍 Distribution Guide

| Distribution | Best starting point |
|---|---|
| Ubuntu | General desktop/server learning |
| Debian | Stable Linux fundamentals |
| Kali Linux | Authorized security labs |
| Fedora | Modern Linux / developer workflows |
| Arch | Deep system learning |
| Alpine | Minimal systems / containers |
| Raspberry Pi OS | Embedded/project learning |
| Termux | Android terminal environment |

Commands can differ between distributions. Always check the local manual:

```bash
man <command>
```

or:

```bash
<command> --help
```

---

# 🗺️ 30-Day Linux Challenge

### Week 1 — Fundamentals

```text
Day 01  Terminal basics
Day 02  Filesystem
Day 03  Files & directories
Day 04  Search tools
Day 05  Permissions
Day 06  Users & groups
Day 07  Review + mini lab
```

### Week 2 — System

```text
Day 08  Processes
Day 09  Services
Day 10  Packages
Day 11  Storage
Day 12  Logs
Day 13  System information
Day 14  Troubleshooting lab
```

### Week 3 — Networking & Shell

```text
Day 15  IP addressing
Day 16  Routes
Day 17  DNS
Day 18  Ports & sockets
Day 19  curl / wget
Day 20  Bash variables
Day 21  Pipes & redirection
```

### Week 4 — Build & Secure

```text
Day 22  Bash scripting
Day 23  Git
Day 24  SSH
Day 25  Firewall concepts
Day 26  Linux hardening
Day 27  Kali fundamentals
Day 28  Termux
Day 29  Build a Linux lab
Day 30  Final project + documentation
```

---

# 🏗️ Final Project Ideas

Choose one and document everything you learned.

### 🟢 Beginner

**Linux Developer Workspace**

- Create a project directory.
- Install Git and Python.
- Write a Bash script.
- Configure Git.
- Create backups.

### 🔵 Intermediate

**Linux Monitoring Dashboard**

Collect:

- CPU
- Memory
- Disk
- Uptime
- Network information
- Process information

### 🟣 Advanced

**Hardened Linux Lab Server**

Practice:

- SSH keys
- Least privilege
- Firewall rules
- Service management
- Log monitoring
- Backups
- Documentation

### 🔴 Security Learning

Build a completely isolated lab with intentionally vulnerable systems and document the defensive lessons learned.

---

# 📖 Useful Documentation

- [Linux man-pages](https://man7.org/linux/man-pages/)
- [GNU Bash Manual](https://www.gnu.org/software/bash/manual/)
- [Debian Documentation](https://www.debian.org/doc/)
- [Ubuntu Documentation](https://documentation.ubuntu.com/)
- [Kali Linux Documentation](https://www.kali.org/docs/)
- [Arch Wiki](https://wiki.archlinux.org/)
- [Termux Wiki](https://github.com/termux/termux-packages/wiki)
- [Git Documentation](https://git-scm.com/doc)

---

# 🤝 Contributing

Contributions are welcome.

You can improve this hub by adding:

- New cheat sheets
- Better explanations
- Distribution-specific notes
- Safe practice labs
- Troubleshooting guides
- Command examples
- Diagrams
- Beginner exercises
- Documentation fixes

### Workflow

```bash
git clone https://github.com/vince551/linux-cheatsheet.git
cd linux-cheatsheet
git switch -c feature/my-improvement
# edit files
git add .
git commit -m "docs: improve Linux learning guide"
git push -u origin feature/my-improvement
```

Then open a Pull Request.

---

# 🔐 Ethics & Responsible Use

This repository is for **education, administration, development and authorized security learning**.

Do not use security techniques against systems, accounts, networks or devices without explicit authorization.

A good security learner should be able to explain both:

```text
HOW a technique works
        +
HOW to detect / prevent / mitigate it
```

**Learn responsibly. Build responsibly. Secure responsibly.**

---

# 👨‍💻 Maintainer

<div align="center">

## VINCE ODHIAMBO

**Full-Stack Developer • Linux Learner • Cybersecurity Enthusiast • Builder**

Building practical projects across software, Linux, networking, cybersecurity and technology.

[![GitHub](https://img.shields.io/badge/GitHub-vince551-181717?style=for-the-badge&logo=github)](https://github.com/vince551)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-00FF88?style=for-the-badge&logo=googlechrome&logoColor=black)](https://portfolio-sage-ten-22.vercel.app/)
[![Instagram](https://img.shields.io/badge/Instagram-vincey.dev-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/vincey.dev)

<br>

> **BUILD • LEARN • SECURE • DESIGN**

⭐ If this hub helps you learn Linux, consider starring the repository.

</div>
