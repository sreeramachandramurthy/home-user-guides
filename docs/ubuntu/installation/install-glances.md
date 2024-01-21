# Glances

## Installation Steps

* Open Terminal
* Install Glances  
  `sudo apt install glances`

## Enable Glances Web UI

The Package version of Glances does not include the Web UI. Copy Web UI JS static files from full version of Glances to the current installed version.

* Open Terminal
* Capture the installed version of Glances  
  `sudo glances -V`
* Export the Glances version to an environmental variable  
  `export GLANCES_VERSION="X.X.X.X"`
* Download full version of Glances  
  `wget https://github.com/nicolargo/glances/archive/refs/tags/v${GLANCES_VERSION}.tar.gz`
* Extract the compressed file  
  `tar zxvf v${GLANCES_VERSION}.tar.gz`
* Copy Web UI JS static files to installation location  
  `sudo cp -r glances-${GLANCES_VERSION}/glances/outputs/static/public/ /usr/lib/python3/dist-packages/glances/outputs/static/`
* Whitelist UI Port  
  `sudo ufw allow 61208/tcp`
* Install optional Plugins  
  `sudo python3 -m pip install pySMART`
* Start Glances  
  `glances -t 300 -w --enable-plugin smart`
* Open Web UI at <http://localhost:61208/>

## Enable Auto Start

* Open Terminal
* Create a service file in `systemd`  
  `sudo vi /etc/systemd/system/glances.service`

```txt
[Unit]
Description=Glances
After=network.target

[Service]
ExecStart=/usr/bin/glances -t 300 -w --enable-plugin smart
Restart=on-abort
RemainAfterExit=yes
localhost
[Install]
WantedBy=multi-user.target
```

* Reload SystemCTL Daemon  
  `sudo systemctl daemon-reload`
* Restart Glances  
  `sudo systemctl start glances`

## Service

* Start the Service  
  `sudo systemctl start glances`
* Restart the Service  
  `sudo systemctl restart glances`
* Stop the Service  
  `sudo systemctl stop glances`
* Enable the Service  
  `sudo systemctl enable glances`
* Status of the Service  
  `sudo systemctl status glances`

## Commands

| Type          | Command                         | Comments       |
| ------------- | ------------------------------- | -------------- |
| Version       | `glances -V`                    |                |
| Web Server    | `glances -w`                    |                |
| Refresh Rate  | `glances -t 5`                  | 5 seconds      |
| Enable Plugin | `glances --enable-plugin smart` | pySMART plugin |

## References

* Glances GitHub - <https://github.com/nicolargo/glances>
* Manual Web UI Installation - <https://github.com/nicolargo/glances/issues/2021>
* Autostart Glances - <https://github.com/nicolargo/glances/wiki/Start-Glances-through-Systemd>
