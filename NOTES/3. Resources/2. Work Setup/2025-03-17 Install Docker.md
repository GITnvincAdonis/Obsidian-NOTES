---
creation date: <% tp.file.creation_date() %>
---

Next, install a few prerequisite packages which let apt use packages over HTTPS:
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

Then add the GPG key for the official Docker repository to your system:
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Add the Docker repository to APT sources:
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```

Make sure you are about to install from the Docker repo instead of the default Ubuntu repo:
```
apt-cache policy docker-ce
```

Finally, install Docker:
```
sudo apt install docker-ce
```


> [!Danger] Verifying Docker works
> ```
> sudo systemctl status docker
> ```


SUDO privileges are optional. Visit documentation for more info 

> [!NOTE] DOCUMENTATION
> https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04#step-1-installing-docker

Link to original: [[2025-03-17 Setup Dev Environment]]
