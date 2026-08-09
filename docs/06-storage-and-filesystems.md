# 06 · Storage & Filesystems

```bash
df -h
du -sh .
du -sh *
lsblk
blkid
findmnt
mount
```

## Mental model
- `lsblk` — block devices
- `findmnt` — mounted filesystems
- `df` — filesystem capacity
- `du` — file/directory usage

> ⚠️ Raw disk, partitioning and formatting commands can destroy data. Verify devices and back up first.
