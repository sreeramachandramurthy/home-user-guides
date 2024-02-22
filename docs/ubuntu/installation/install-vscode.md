# Install VS Code

## Installation Steps

### Through APT

Open Terminal and execute the below commands to install Visual Studio Code through APT

* Install Dependencies

```bash
sudo apt-get install wget gpg
```

* Download Keys

```bash
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
```

* Install Keys

```bash
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
```

* Add APT Repository

```bash
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
```

* Clean Up Keys

```bash
rm -f packages.microsoft.gpg
```

* Install Dependencies

```bash
sudo apt install apt-transport-https
```

* Update Package Cache

```bash
sudo apt update
```

* Install VS Code

```bash
sudo apt install code
```

### Through DEB Package

* Download the DEB package from [https://code.visualstudio.com/download](https://code.visualstudio.com/download 'VS Code Download')
* Open Terminal and navigate to the downloaded path
* Run the below command to install from the downloaded DEB file

```bash
sudo apt install ./<filename.deb>`
```
