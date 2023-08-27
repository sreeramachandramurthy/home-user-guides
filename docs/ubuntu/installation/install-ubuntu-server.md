# Migrate from Ubuntu Desktop to Ubuntu Server

## Steps

* Open Terminal
* Run `sudo apt install ubuntu-server`
* Run `reboot`
* Run `sudo systemctl set-default multi-user.target`
* Run `reboot`
* Run `sudo apt purge ubuntu-desktop -y && sudo apt autoremove -y && sudo apt autoclean`
* Run `reboot`
