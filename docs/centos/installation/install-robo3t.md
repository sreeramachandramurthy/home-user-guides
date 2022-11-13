# Install Robo3T

## Installation Steps

* Create a directory for Robo 3T software
`sudo mkdir /opt/robo3t`
* Download Robo3T from [Robo3T website](https://robomongo.org/download). Alternatively, you can use `wget`
`wget https://download.studio3t.com/robomongo/linux/robo3t-1.4.3-linux-x86_64-48f7dfd.tar.gz`
* Extract the downloaded tarball to the Robo3T directory `/opt/robo3t`
`sudo tar xf robo3t-1.4.3-linux-x86_64-48f7dfd.tar.gz -C /opt/robo3t --strip-component=1`
* Create symbolic links for Robo3T executable, so it can be run from anywhere
`sudo ln -s /opt/robo3t/bin/robo3t /usr/local/bin/robo3t`

## Running Robo3T

* Open Terminal
* Run `robo3t`

> If you are running Robo 3T on a headless server then you have to configure x11 forwarding with PuTTY and XMing to get the GUI output on to your client machine.

## Workaround for CentOS

Robo 3T 1.4.x fails to run in CentOS with the below error. The linux version of Robo3T supports only Ubuntu. To run on CentOS, execute the following commands in a new Terminal.

> robo3t: error while loading shared libraries: libcurl-gnutls.so.4: cannot open shared object file: No such file or directory

* Search for the packages having `libcurl.so.4` library `yum whatprovides */libcurl.so.4`
* Install `libcurl`
`sudo yum install libcurl`
* It gets installed into `/usr/lib64`
* Copy the missing library to Robo 3T directory
`sudo cp /usr/lib64/libcurl.so.4 /opt/robo3t/lib/libcurl-gnutls.so.4`
* Run Robo 3T
`robo3t`

## Add Robo3T to Applications

* Download any Robo3T icon from Google Images and copy it to the `bin` directory of Robo 3T
`cp robo3t.png /opt/robo3t/bin/robo3t.png`
* Create a new desktop file
`sudo vi /usr/share/applications/Robo3T.desktop`
* Add the following content to the file

```bash
[Desktop Entry]
Version=1.4.3
Name=Robo3T
Exec=/opt/robo3t/bin/robo3t
Terminal=false
Type=Application
StartupNotify=true
Categories=Development;
Icon=/opt/robo3t/bin/robo3t.png
X-Desktop-File-Install-Version=0.15
```
