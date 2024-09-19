# Ubuntu Server

Migrate from Ubuntu Desktop to Ubuntu Server

## Steps

* Open Terminal
* Install Ubuntu Server  
  `sudo apt install ubuntu-server`
* Reboot the Server  
  `reboot`
* Enable Multi User  
  `sudo systemctl set-default multi-user.target`
* Reboot the Server  
  `reboot`
* Remove Ubunut Desktop  
  `sudo apt purge ubuntu-desktop -y && sudo apt autoremove -y && sudo apt autoclean`
* Reboot the Server  
  `reboot`
