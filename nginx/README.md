# NGINX

## Instalation

- https://www.nginx.com/resources/wiki/start/topics/tutorials/install/

```sh
$ sudo -s
$ nginx=stable # use nginx=development for latest development version
$ add-apt-repository ppa:nginx/$nginx
$ apt-get update
$ apt-get install nginx
$ nginx
$ systemctl status nginx
```

- Folder nginx: /usr/share/nginx/html

- Docker

```sh
# The :ro option causes these directors to be read only inside the container.
$ docker run --name mynginx2 -v ~/volumes/nginx:/usr/share/nginx/html:ro -P -d nginx
```
