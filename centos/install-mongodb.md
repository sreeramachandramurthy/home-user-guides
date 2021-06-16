# Install MongoDB

## Installation

`sudo vi /etc/yum.repos.d/mongodb-org.repo`

```txt
[mongodb-org-4.2]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/4.2/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.2.asc
```

`yum repolist`

`sudo yum install mongodb-org`

## Service

`sudo systemctl enable mongod`

`sudo systemctl start mongod`

`sudo systemctl reload mongod`

`sudo systemctl stop mongod`

## Logs

`sudo tail /var/log/mongodb/mongod.log`

## Firewall

`sudo firewall-cmd --zone=public --add-port=27017/tcp --permanent`

`sudo firewall-cmd --reload`

## Process

`ps -ef | grep mongo`

`netstat -an | grep 27017`

## References

- [MongoDB Docs](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-red-hat/)
