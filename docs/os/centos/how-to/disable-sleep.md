# Disable Sleep when Laptop lid is closed

* Open Terminal
* Edit file `vi /etc/systemd/logind.conf`

```txt
HandleLidSwitch=ignore
```

* Restart service `systemctl restart systemd-logind`
