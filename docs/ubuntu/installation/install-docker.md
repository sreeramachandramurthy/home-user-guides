# Install Docker CE

## Install using the apt Repository

Before you install Docker Engine for the first time on a new host machine, you need to set up the Docker repository. Afterward, you can install and update Docker from the repository.

### Set up the Repository

Update the apt package index and install packages to allow apt to use a repository over HTTPS

* Open Terminal
    * Run `sudo apt-get update`
    * Run `sudo apt-get install ca-certificates curl gnupg`
* Add Docker’s official GPG key
    * Run `sudo install -m 0755 -d /etc/apt/keyrings`
    * Run `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg`
    * Run `sudo chmod a+r /etc/apt/keyrings/docker.gpg`
* Set up the Repository
    * Run `echo "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`

### Install Docker Engine

* Open Terminal
* Run `sudo apt-get update`
* To install the latest version, run  
  `sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`

### Verify Installation

* To verify that the Docker Engine installation is successful, run the `hello-world` image.  
  `sudo docker run hello-world`

### Start on Boot

Configure Docker to start on boot

* Open Terminal
* Run `sudo systemctl enable docker.service`
* Run `sudo systemctl enable containerd.service`

To disable this behavior, use disable instead.

* Run `sudo systemctl disable docker.service`
* Run `sudo systemctl disable containerd.service`

## References

* <https://docs.docker.com/engine/install/ubuntu/>
* <https://docs.docker.com/engine/install/linux-postinstall/>
