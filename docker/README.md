# Docker

## Instalation

Linux installation (easy way)

```sh
$ curl -sSL https://get.docker.com/ | sh
```

## Portainer

```sh
$ docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v /home/ramuspedro/Desenvolvimento/Portainer/data:/data portainer/portainer
```
