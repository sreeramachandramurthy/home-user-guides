# Glances

## Installation Steps

* Open Terminal
* Run `sudo apt-get install glances`

## Enable Glances Web UI

The Package version of Glances does not include the Web UI. Copy Web UI JS static files from full version of Glances to the current installed version.

* Open Terminal
* Capture the installed version of Glances `sudo glances -V`
* Export the version to an environmental variable `export GLANCES_VERSION="X.X.X.X"`
* Download full version of Glances `wget https://github.com/nicolargo/glances/archive/refs/tags/v${GLANCES_VERSION}.tar.gz`
* Extract the compressed file `tar zxvf v${GLANCES_VERSION}.tar.gz`
* Copy Web UI JS static files to installation location `sudo cp -r glances-${GLANCES_VERSION}/glances/outputs/static/public/ /usr/lib/python3/dist-packages/glances/outputs/static/`
* Open Web UI at `http://localhost:61208`

## Enable Auto Start

* Open Terminal
* Create a service file in `systemd`  
  `sudo vi /etc/systemd/system/glances.service`

```txt
[Unit]
Description=Glances
After=network.target

[Service]
ExecStart=/usr/local/bin/glances -t 300 -w
Restart=on-abort
RemainAfterExit=yes

[Install]
WantedBy=multi-user.target
```

* Reload

```bash
sudo systemctl daemon-reload
sudo systemctl stop glances.service
sudo systemctl start glances.service
sudo systemctl status glances.service
sudo systemctl enable glances.service
```

## Commands

| Type         | Command                  |
| ------------ | ------------------------ |
| Version      | `glances -V`             |
| Web Server   | `glances -w`             |
| Refresh Rate | `glances -t 5` 5 seconds |

## References

* Glances GitHub - <https://github.com/nicolargo/glances>
* Manual Web UI Installation - <https://github.com/nicolargo/glances/issues/2021>
* Autostart Glances - <https://github.com/nicolargo/glances/wiki/Start-Glances-through-Systemd>
