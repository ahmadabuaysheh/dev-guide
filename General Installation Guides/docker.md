# Install docker and docker-compose

Uninstall old versions of Docker
```
sudo apt-get remove docker docker.io containerd runc docker-engine
```

### Update the apt package index
```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```

### Add Docker’s official GPG key:
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

### Verify
```
sudo apt-key fingerprint 0EBFCD88
```

```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

If you are using a very recent release of Ubuntu and docker didn't release a special directory for it use the name of the last release; in our case it is eoan (Ubuntu 19.10)
```
   sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   eoan \
   stable"
```

```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```


Reboot your system and Enable Docker
```
sudo systemctl enable --now docker
```

give your username admin privileges to docker to run it without sudo

```
sudo usermod -aG docker $USER
newgrp docker
```

Check docker now
```
docker --version
```

Install docker-compose, replace 1.25.5 with any version
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

```

Apply excutable to the docker-compose file
```
sudo chmod +x /usr/local/bin/docker-compose
```