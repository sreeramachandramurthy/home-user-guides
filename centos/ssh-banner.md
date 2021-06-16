# Customizing SSH Banner Message

Open Terminal and run the following commands

`vi /etc/greetings.txt`

```txt
#####################################
#    WELCOME TO RAM-SERVER          #
#####################################
```

`vi /etc/ssh/sshd_config`

```txt
Banner /etc/greetings.txt
```

`systemctl restart sshd`
