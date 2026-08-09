# 15 · Termux & Mobile Linux

Termux provides a terminal environment on Android. It is not identical to a conventional desktop Linux distribution.

## Start
```bash
pkg update
pkg upgrade
pkg install git
pkg install python
termux-setup-storage
```

## Understand the stack
```text
Android kernel
   ↓
Termux app
   ↓
Termux userland
   ↓
Optional proot/container-like environments
```

Architecture, Android permissions and kernel restrictions determine what can run. Never assume a desktop Linux command will behave identically on Android.
