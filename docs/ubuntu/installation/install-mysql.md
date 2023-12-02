# Install MySQL

## Installation Steps

* Open Terminal
* Run `sudo apt install mysql-server`
* Run `mysql --version`
* Run `sudo mysql_secure_installation`
* Run `sudo systemctl status mysql`

* `sudo mysql -u root`
* `ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password BY 'yourpasswd';`

changing bind-address 127.0.0.1 to bind-address 0.0.0.0 in /etc/mysql/mysql.conf.d so that MySQL listens on all ports.