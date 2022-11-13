# Configure Static IP Address in CentOS

* Open Terminal
* Navigate to the Network Scripts

    `cd /etc/sysconfig/network-scripts`

* Edit file `vi ifcfg-eth0` (or respective network adapter)

```txt
ONBOOT=yes
BOOTPROTO=static
IPADDR=10.0.0.22
NETMASK=255.255.255.0
GATEWAY=10.0.0.1
DNS1=10.0.0.1
```

* Restart service `service network restart`
* Confirm changes by running `ifconfig`
