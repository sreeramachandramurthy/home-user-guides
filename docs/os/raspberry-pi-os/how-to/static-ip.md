# Static IP

* Enable Manual interaction for Ethernet  
  `/etc/network/interfaces`

  ```txt
  iface eth0 inet manual
  ```

  or

  ```txt
  iface eth0 inet static
  ```

sudo apt install dhcpcd

sudo vi /etc/dhcpcd.conf 
interface eth0 
static ip_address=10.0.0.40/24
static routers=10.0.0.1
static domain_name_servers=10.0.0.1


* Restart the Raspberry Pi  
  `sudo reboot`
