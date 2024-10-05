# Install Portainer CE

## Prerequisites

* The latest version of Docker installed and working.
* `sudo` access on the machine that will host your Portainer Server instance.

## Installation Steps

* Open Terminal
* Create volume for Portainer Server

```bash
docker volume create portainer-data
```

* Download and install the Portainer Server container

```bash
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer-data:/data portainer/portainer-ce:2.21.2
```

* Verify installation

```bash
docker ps
```

## References

1. <https://docs.portainer.io/start/install-ce/server/docker/linux>
