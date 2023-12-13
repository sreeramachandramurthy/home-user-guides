# Install Mosquitto

## Installation Steps

* Open Terminal
* Add Mosquitto repository  
  `sudo add-apt-repository ppa:mosquitto-dev/mosquitto-ppa`
* Install Mosquitto  
  `sudo apt install mosquitto`
* Check Mosquitto version  
  `mosquitto -version`
* Remove anonymous access (create an account)  

```bash
sudo mosquitto_passwd -c /etc/mosquitto/passwd <username>
Password:
Reenter password:
```

* Update the default configuration at `/etc/mosquitto/conf.d/default.conf`  

```txt
listener 1883
password_file /etc/mosquitto/passwd
```

* Update the file permissions for the password file  
  `sudo chmod 666 etc/mosquitto/passwd`
* Restart the Mosquitto service  
  `sudo systemctl restart mosquitto`

## Service

* Start the Service  
  `sudo service mosquitto start`
* Restart the Service  
  `sudo service mosquitto restart`
* Stop the Service  
  `sudo service mosquitto stop`
* Enable the Service  
  `sudo systemctl enable mosquitto`
