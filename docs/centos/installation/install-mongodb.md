# Install MongoDB

## Installation Steps

### Add MongoDB Repo

* Open Terminal
* Run `sudo vi /etc/yum.repos.d/mongodb-org.repo`
* Add the below text to the file

```txt
[mongodb-org-4.2]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/4.2/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.2.asc
```

### Install Mongo DB

* Run `yum repolist`
* `sudo yum install mongodb-org`

## Configuration

* Open Terminal
* Edit MongoDB configuration file
`vi /etc/mongod.conf`
* Change `bindIp` to the ip address of the machine.

## Service

* Open Terminal
* Run `sudo systemctl enable mongod` to add the MongoDB service to StartUp
* Run `sudo systemctl start mongod` to start MongoDB service
* Run `sudo systemctl restart mongod` to restart MongoDB service
* Run `sudo systemctl stop mongod` to stop MongoDB service

## Logs

* Open Terminal
* Run `sudo tail /var/log/mongodb/mongod.log`

## Firewall

* Run `sudo firewall-cmd --zone=public --add-port=27017/tcp --permanent` to open port `27017`
* Run `sudo firewall-cmd --reload` to reload firewall service

## Process

* Open Terminal
* Run `ps -ef | grep mongo`
* Run `netstat -an | grep 27017`

## References

* [MongoDB Docs](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-red-hat/)
* [MongoDB 4.2 Docs](https://docs.mongodb.com/v4.2/tutorial/install-mongodb-on-red-hat/)
