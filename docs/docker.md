# Docker

Two step process:

1. Set up the Docker repository
2. Install and update Docker from the repository.

## Set up repository

Update the apt package index and install packages to allow apt to use a repository over HTTPS:

```{bash}
$ sudo apt-get update

$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```

Likely all of the above is already installed.

Add Docker’s official GPG key:

```{bash}
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

```

Verify that you now have the key with the fingerprint 9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88, by searching for the last 8 characters of the fingerprint.

```{bash}
$ sudo apt-key fingerprint 0EBFCD88

pub   rsa4096 2017-02-22 [SCEA]
      9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
uid           [ unknown] Docker Release (CE deb) <docker@docker.com>
sub   rsa4096 2017-02-22 [S]
```

Now add the repository:

```{bash}
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

## Install Docker Engine

Update the apt package index, and install the latest version of Docker Engine and containerd

```{bash}
 $ sudo apt-get update
 $ sudo apt-get install docker-ce docker-ce-cli containerd.io
```

## Verify Installation:

```{bash}
$ sudo docker run hello-world
```