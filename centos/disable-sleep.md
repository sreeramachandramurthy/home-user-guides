# Disable Sleep when Laptop lid is closed

Open Terminal and run the following commands

`vi /etc/systemd/logind.conf`

```txt
HandleLidSwitch=ignore
```

`systemctl restart systemd-logind`
