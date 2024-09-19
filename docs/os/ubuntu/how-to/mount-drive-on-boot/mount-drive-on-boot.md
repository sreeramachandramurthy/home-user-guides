# How to Mount Drive on Boot

## Overview

When we connect an external drive, by default, Linux OS (or Ubuntu Server) doesn't automount the external drive at startup. We can mount the drive using the `mount` command manually but we can also enable automount feature on startup. This feature avoids us to mount the drive again after restarting or logging into Linux OS.

## Steps

* Create a directory for mounting the attached drive  
  > Normally mount directories are created in `/media`  

```bash
sudo mkdir /media/ram/caddy
```

* Get the attached drive's UUID and and File System Type

```bash
lsblk -o NAME,FSTYPE,UUID,MOUNTPOINTS
```

* Edit `fstab` to add attached drive's details

```bash
sudo vi /etc/fstab
```

* Add entry for the attached drive  
  > Values are seperated by `TAB`

```txt
UUID=xxxx-xxxx-xxxx-xxxx-xxxx    /media/ram/caddy    ext4    defaults    0    0
```

* Test `fstab`  
  > Test `fstab` before rebooting as an invalid `fstab` can render a disk unbootable

```bash
sudo findmnt --verify
```

* Restart Ubuntu

```bash
sudo reboot
```

## References

1. <https://developerinsider.co/auto-mount-drive-in-ubuntu-server-22-04-at-startup/>
