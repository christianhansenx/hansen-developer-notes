# Linux systemd

## temporary file system (tmpfs) for the /tmp directory

Check current file system: ```df -Th /tmp```
```
Filesystem     Type  Size  Used Avail Use% Mounted on
/dev/mmcblk0p2 ext4   28G  2.5G   25G  10% /
```
*Example from RPI3 where tmp is not tmpfs"*

Change it to tmpfs
```
sudo cp /usr/share/systemd/tmp.mount /etc/systemd/system/tmp.mount
sudo systemctl enable tmp.mount
sudo systemctl start tmp.mount
```

Use ```systemctl edit tmp.mount``` to specify a different size, for example size=2G for a 2GB