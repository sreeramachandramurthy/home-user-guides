# Install Docker CE

## Direct Installation

Install and update Docker from the YUM repository

### Setup the YUM Repository

* Install the `yum-utils` package (which provides the `yum-config-manager` utility) and set up the repository

    `sudo yum install -y yum-utils`

* Run `sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo`

### Install Docker Engine

* Install the latest version of Docker Engine and containerd

    `sudo yum install docker-ce docker-ce-cli containerd.io`

If prompted to accept the GPG key, verify that the fingerprint matches `060A 61C5 1B55 8A7F 742B 77AA C52F EB6B 621E 9F35`, and if so, accept it.

Docker is installed but not started. The `docker` group is created, but no users are added to the group.

### Start Docker

* Run `sudo systemctl start docker`

### Verify Docker Engine

* Run `sudo docker run hello-world`

This command downloads a test image and runs it in a container. When the container runs, it prints an informational message and exits.

Docker Engine is installed and running. You need to use `sudo` to run Docker commands.

## Post Installation

The Docker daemon binds to a Unix socket instead of a TCP port. By default that Unix socket is owned by the user `root` and other users can only access it using `sudo`. The Docker daemon always runs as the `root` user.

If you don’t want to preface the `docker` command with `sudo`, create a Unix group called `docker` and add users to it. When the Docker daemon starts, it creates a Unix socket accessible by members of the `docker` group.

### Create the Docker Group

* Run `sudo groupadd docker`

### Add User to the Docker Group

* Run `sudo usermod -aG docker $USER`

Log out and log back in so that your group membership is re-evaluated.

* If testing on a virtual machine, it may be necessary to restart the virtual machine for changes to take effect.
* On a desktop Linux environment such as X Windows, log out of your session completely and then log back in.
* On Linux, you can also run the following command to activate the changes to groups

    `newgrp docker`

### Verify

Verify that you can run docker commands without `sudo`.

    `docker run hello-world`

This command downloads a test image and runs it in a container. When the container runs, it prints an informational message and exits.

> If you initially ran Docker CLI commands using `sudo` before adding your user to the docker group, you may see the following error, which indicates that your `~/.docker/` directory was created with incorrect permissions due to the `sudo` commands.

```bash
WARNING: Error loading config file: /home/user/.docker/config.json -
stat /home/user/.docker/config.json: permission denied
```

To fix this problem, either remove the `~/.docker/` directory (it is recreated automatically, but any custom settings are lost), or change its ownership and permissions using the following commands:

```bash
sudo chown "$USER":"$USER" /home/"$USER"/.docker -R
sudo chmod g+rwx "$HOME/.docker" -R
```

## Start on Boot

Configure Docker to start on boot

```bash
sudo systemctl enable docker.service
sudo systemctl enable containerd.service
```

To disable this behavior, use disable instead.

```bash
sudo systemctl disable docker.service
sudo systemctl disable containerd.service
```

## Uninstall Docker Engine

To uninstall the Docker Engine, CLI, and Containerd packages, run the below command

    `sudo yum remove docker-ce docker-ce-cli containerd.io`

Images, containers, volumes, or customized configuration files on your host are not automatically removed. To delete all images, containers, and volumes, run the below command

```bash
sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd
```

You must delete any edited configuration files manually.

## References

* [Install Docker CE on CentOS](https://docs.docker.com/engine/install/centos/)
* [Post Install on Linux](https://docs.docker.com/engine/install/linux-postinstall/)
