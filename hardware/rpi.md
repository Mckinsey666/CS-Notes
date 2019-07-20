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

## Installing node on RPi
First find the relevant resource file url (at the **Node.js distribution repository**). Suppose it be `https://nodejs.org/dist/v9.0.0/node-v9.9.0-linux-armv6l.tar.gz`.
```
curl -o node-v9.9.0-linux-armv6l.tar.gz https://nodejs.org/dist/v9.9.0/node-v9.9.0-linux-armv6l.tar.gz
```
```
tar -xzf node-v9.9.0-linux-armv6l.tar.gz
```
```
sudo cp -r node-v9.9.0-linux-armv6l/* /usr/local/
```
