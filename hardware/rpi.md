# RPi 

## Backing Up a Raspberry Pi SD card
Use `dd` command on Linux.
1. Check SD card location.
```
sudo fdisk -l
```

2. Backup system data (suppose system data is in `/dev/mmcblk0`)
```
sudo dd bs=4M if=/dev/mmcblk0 | gzip > filename.zip
```
To show backup status, add `status=progress` flag.