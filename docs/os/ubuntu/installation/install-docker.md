# Install Docker CE

## Install using the APT Repository

Before you install Docker Engine for the first time on a new host machine, you need to set up the Docker repository. Afterward, you can install and update Docker from the repository.

### Set up the Repository

* Open Terminal
* Update Ubuntu

```bash
sudo apt update
```

* Install dependant packages

```bash
sudo apt install ca-certificates curl gnupg
```

* Add Docker’s official GPG key

```bash
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

* Add the Repository

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
```

### Install Docker Engine

* Open Terminal
* To install the latest version, run

```bash
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### Verify Installation

* To verify that the Docker Engine installation is successful, run the `hello-world` image.

```bash
sudo docker run hello-world
```

### Manage Docker as a non-root User

The Docker daemon binds to a Unix socket, not a TCP port. By default it's the `root` user that owns the Unix socket, and other users can only access it using `sudo`. The Docker daemon always runs as the `root` user.

If you don't want to preface the `docker` command with sudo, create a Unix group called `docker` and add users to it. When the Docker daemon starts, it creates a Unix socket accessible by members of the `docker` group. On some Linux distributions, the system automatically creates this group when installing Docker Engine using a package manager. In that case, there is no need for you to manually create the group.

* Create the Docker group

```bash
sudo groupadd docker
```

* Add user to the Docker group

```bash
sudo usermod -aG docker $USER
```

* Activate the changes to the groups

```bash
newgrp docker
```

* Verify that you can run `docker` commands without `sudo`.

```bash
docker run hello-world
```

### Start on Boot

Configure Docker to start on boot

* Open Terminal
* Run the below commands

```bash
sudo systemctl enable docker.service
sudo systemctl enable containerd.service
```

To disable this behavior, use disable instead.

```bash
sudo systemctl disable docker.service
sudo systemctl disable containerd.service
```

## References

* <https://docs.docker.com/engine/install/ubuntu/>
* <https://docs.docker.com/engine/install/linux-postinstall/>
