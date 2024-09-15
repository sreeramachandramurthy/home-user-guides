# How to Mount Drive on Boot

## Steps

* Create a directory for mounting the attached drive

```bash
sudo mkdir /media/ram/caddy
```

* Get the attached drive's UUID and Type

```bash
lsblk -o NAME,FSTYPE,UUID,MOUNTPOINTS
```

* Edit `fstab` to add attached drive's details

```bash
sudo vi /etc/fstab
```

* Add entry for the attached drive

```txt
UUID=xxxx-xxxx-xxxx-xxxx-xxxx    /media/ram/caddy    ext4    defaults    0    0
```

* Test `fstab`  
  Test `fstab` before rebooting as an invalid `fstab` can render a disk unbootable

```bash
sudo findmnt --verify
```

* Restart Ubuntu

```bash
sudo reboot
```

## References

1. <https://developerinsider.co/auto-mount-drive-in-ubuntu-server-22-04-at-startup/>
