# Configure Static IP Address in CentOS

Open Terminal and run the following commands

`cd /etc/sysconfig/network-scripts`

`vi ifcfg-eth0` (or respective network adapter)

```txt
ONBOOT=yes
BOOTPROTO=static
IPADDR=10.0.0.22
NETMASK=255.255.255.0
GATEWAY=10.0.0.1
```

`service network restart`

`ifconfig`
