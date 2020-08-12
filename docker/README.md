# Docker

## Instalation

Linux installation (easy way)

```sh
$ curl -sSL https://get.docker.com/ | sh

# if you got a permission error
$ sudo chmod 777 /var/run/docker.sock

# if want docker-compose as well
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.26.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

$ sudo chmod +x /usr/local/bin/docker-compose

$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

## Portainer

```sh
$ docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v /home/ramuspedro/Desenvolvimento/Portainer/data:/data portainer/portainer
```

## Docker Swarm

```sh
$ docker swarm init --advertise-addr 127.0.0.1
``` 