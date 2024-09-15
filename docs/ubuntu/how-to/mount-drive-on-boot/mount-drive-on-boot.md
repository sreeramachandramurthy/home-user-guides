# How to Mount Drive on Boot

## Steps

* Create a directory for mounting the attached drive

```bash
sudo mkdir /media/ram/caddy
```

* Get drive UUID and Type

```bash
lsblk -o NAME,FSTYPE,UUID,MOUNTPOINTS
```

* Edit `fstab` to add drive details

```bash
sudo vi /etc/fstab
```

* Add entry for drive

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
