# dockerizing-examples
A repository with examples applications dockerizations using docker-compose

# Installing Docker

## Ubuntu, Mint

Uninstall old versions:

```sudo apt-get remove docker docker-engine docker.io containerd runc```

Update package index

```sudo apt-get update```

Install packages to allow apt to use a repository over HTTPS:

```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```

Add Docker’s official GPG key:

```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -```


Set up the stable repository **for your system**:

- Ubuntu 18.04/Mint 19, 19.1 and 19.2

```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   bionic \
   stable"
```

Update package index:

```
sudo apt-get update
```

Install the latest version of Docker Engine

```
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

Verify that Docker Engine:

```
sudo docker run hello-world
```


Create the docker group:

```
sudo groupadd docker
```

Add your user to the docker group:

```
sudo usermod -aG docker $USER
```

Log out and back, or, in linux, activate the changes:

```
newgrp docker
```

Verify you can run docker commands without sudo:

```
docker run hello-world
```

Get current stable version of composer:

```
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Applly executable permissions:

```
sudo chmod +x /usr/local/bin/docker-compose
```

Test installation:

```
docker-compose --version
```