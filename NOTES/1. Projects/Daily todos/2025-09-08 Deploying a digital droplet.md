---
creation date: <% tp.file.creation_date() %>
---

> [!Danger] Requirements
> #### - DOMAIN (CloudFlair for deplyoments, DUCK DNS for testing)
> #### - KAMAL
> #### - Digital ocean account

#### Process:
Kamal is essentially a wrapper around different docker commands.
The process envolves: 
- Creating docker image (using dockerfile)
- Pushing image to a registry
- SSHing into provided VM 
- Pulling docker image from the registry
- Running docker container


This highlights the need for the following parts:
- Authentication into VM, Rails APP, and docker registry. SSH keys on the system deal with authenticating into VM (generated and saved during VM setup). Rails and docker registry use the kamal secrets key. BE SURE TO ADD SECRETS TO GITIGNORE. Docker hub is the default registry. A personal access key must be generated and saved for the docker hub account to allow for registry authentication, allowing pulling of docker images while in the server.
   
- IP addresses for VM and Domain host.

### DOMAIN
set Domain to point to VM public IP




#### Common Errors:

**Kamal lock in place**

Simply disable lock:

```
kamal lock releasse
```

**permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock**

This just means that the user  doesn't have permission to use docker. Add 
them to the trusted Groups:
   
```
sudo usermod -aG docker $USER
```

this assumes that the following returns a permission denied:

```
docker ps
```

**dial tcp [2600:1f18:2148:bc02:...]:443: connect: network is unreachable**

Typically means there is an error accessing docker hub (a docker registry) over a IP6 connection. To fix, configure docker to use an IP4 connection:

Create or edit the Docker daemon configuration:
```
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<EOF
{
  "ipv6": false,
  "dns": ["8.8.8.8", "1.1.1.1"]
}
EOF
```


Debugging resources:

[KAMAL Unpacked](https://www.youtube.com/watch?v=sPUk9-1WVXI)
[Kamal Documentation](https://kamal-deploy.org/)

Link to original: [[2025-09-08]]