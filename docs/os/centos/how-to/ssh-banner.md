# Customizing SSH Banner Message

* Open Terminal
* Edit file `vi /etc/greetings.txt`

```txt
#####################################
#    WELCOME TO RAM-SERVER          #
#####################################
```

* Edit file `vi /etc/ssh/sshd_config`

```txt
Banner /etc/greetings.txt
```

* Restart service `systemctl restart sshd`
