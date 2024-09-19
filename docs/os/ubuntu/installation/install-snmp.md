# Install SNMP

sudo apt-get update
sudo apt-get install snmpd
sudo nano /etc/snmp/snmpd.conf
    agentAddress udp:161,udp6:[::1]:161
    rocommunity public
sudo service snmpd restart
sudo service snmpd status


Install the tools

sudo apt-get install snmp-mibs-downloader

SNMP usage

snmpwalk -c public -v1 localhost | less