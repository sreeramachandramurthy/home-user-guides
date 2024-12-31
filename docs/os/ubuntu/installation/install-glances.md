# Glances

## Installation Steps

Open Terminal and execute the below commands to install Glances through PipX

* Install dependant packages

```bash
sudo apt install python3 python3-pip pipx
pipx ensurepath
```

* Close and re-open Terminal
* Install Glances with PipX

```bash
pipx install 'glances[all]'
```

## Enable Auto Start

Open Terminal and execute the below commands to enable Glances to start after system boot

* Create a service file in `systemd`

```bash
sudo vi /etc/systemd/system/glances.service
```

```txt
[Unit]
Description=Glances
After=network.target

[Service]
ExecStart=/home/${USER}/.local/bin/glances -t 300 -w
Restart=on-abort
RemainAfterExit=yes

[Install]
WantedBy=multi-user.target
```

* Reload SystemCtl Daemon

```bash
sudo systemctl daemon-reload
```

* Start Glances

```bash
sudo systemctl start glances
```

* Enable the Service

```bash
sudo systemctl enable glances
```

## Whitelist UI Port

Open Terminal and execute the below commands to open ports for accessing the Web UI in external systems

```bash
sudo ufw allow 61208/tcp
```

## Web UI

* Open Glances Web UI at <http://localhost:61208/>

## Commands

### Service Commands

| Type          | Command                         | Comments       |
| ------------- | ------------------------------- | -------------- |
| Version       | `glances -V`                    |                |
| Web Server    | `glances -w`                    |                |
| Refresh Rate  | `glances -t 5`                  | 5 seconds      |
| Enable Plugin | `glances --enable-plugin smart` | pySMART plugin |

### SystemCtl Commands

| Type                    | Command                          | Comments       |
| ----------------------- | -------------------------------- | -------------- |
| Start the Service       | `sudo systemctl start glances`   |                |
| Stop the Service        | `sudo systemctl stop glances`    |                |
| Restart the Service     | `sudo systemctl restart glances` |                |
| Enable the Service      | `sudo systemctl enable glances`  |                |
| Status of the Service   | `sudo systemctl status glances`  |                |

## References

* Glances GitHub - <https://github.com/nicolargo/glances>
* Manual Web UI Installation - <https://github.com/nicolargo/glances/issues/2021>
* Autostart Glances - <https://github.com/nicolargo/glances/wiki/Start-Glances-through-Systemd>
