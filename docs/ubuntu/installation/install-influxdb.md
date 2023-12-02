# Install InfluxDB

## Install InfluxDB as a Service

* Update the Ubuntu System  
  `sudo apt update`
* Get Packages for Ubuntu  

```bash
wget -q https://repos.influxdata.com/influxdata-archive_compat.key

echo '393e8779c89ac8d958f81f942f9ad7fb82a25e133faddaf92e15b16e6ac9ce4c influxdata-archive_compat.key' | sha256sum -c && cat influxdata-archive_compat.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/influxdata-archive_compat.gpg > /dev/null

echo 'deb [signed-by=/etc/apt/trusted.gpg.d/influxdata-archive_compat.gpg] https://repos.influxdata.com/debian stable main' | sudo tee /etc/apt/sources.list.d/influxdata.list
```

* Update the Ubuntu System  
  `sudo apt update`
* Install InfluxDB  
  `sudo apt install influxdb2`
* Check Version of InfluxDB  
  `influx version`
* Start the InfluxDB as a Service  
  `sudo systemctl start influxdb`
* Enable InfluxDB as a Service  
  `sudo systemctl enable influxdb`
* Verify the InfluxDB Installation  
  `sudo service influxdb status`

## Config the InfluxDB

* Start the Service  
  `sudo service influxdb start`
* Restart the Service  
  `sudo service influxdb restart`
* Stop the Service  
  `sudo service influxdb stop`

## Config Firewall

* Whitelist InfluxDB in Firewall  
  `sudo ufw allow 8086/tcp`

## GUI

<http://localhost:8086>
