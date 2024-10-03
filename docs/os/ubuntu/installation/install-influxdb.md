# Install InfluxDB

## Install InfluxDB as a Service

* Open Terminal
* Update the Ubuntu System

```bash
sudo apt update
```

* Add the GPG fingerprint

```bash
wget -q https://repos.influxdata.com/influxdata-archive_compat.key`
echo '393e8779c89ac8d958f81f942f9ad7fb82a25e133faddaf92e15b16e6ac9ce4c influxdata-archive_compat.key' | sha256sum -c && cat influxdata-archive_compat.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/influxdata-archive_compat.gpg > /dev/null
```

* Add the InfluxDB to the repository list

```bash
echo 'deb [signed-by=/etc/apt/trusted.gpg.d/influxdata-archive_compat.gpg] https://repos.influxdata.com/debian stable main' | sudo tee /etc/apt/sources.list.d/influxdata.list
```

* Update the Ubuntu System

```bash
sudo apt update
```

* Install InfluxDB

```bash
sudo apt install influxdb
```

* Check Version of InfluxDB

```bash
influx -version
```

* Start the InfluxDB as a Service

```bash
sudo systemctl start influxdb
```

* Verify the InfluxDB installation

```bash
sudo service influxdb status
```

## Config InfluxDB

* Start the Service

```bash
sudo service influxdb start
```

* Restart the Service

```bash
sudo service influxdb restart
```

* Stop the Service

```bash
sudo service influxdb stop
```

* Enable the Service

```bash
sudo systemctl enable influxdb
```

## Config Firewall

* Whitelist InfluxDB in Firewall

```bash
sudo ufw allow 8086/tcp
```

## References

1. <https://docs.influxdata.com/influxdb/v1/introduction/install/>
