# Install Docker Compose

## Table of Contents

1. [Installation](#installtion)
1. [Uninstallation](#uninstalltion)

## Installation

Download the current stable release of Docker Compose:

`sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`

Apply executable permissions to the binary

`sudo chmod +x /usr/local/bin/docker-compose`

Check version

`docker-compose --version`

## Uninstallation

To uninstall Docker Compose

`sudo rm /usr/local/bin/docker-compose`
