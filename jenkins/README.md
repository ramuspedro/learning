# Jenkins

## Installation

### Docker

```sh
# Permission on cloud to access a specific folder
$ docker run --name myjenkins -p 8080:8080 -p 50000:50000 -v jenkins:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock jenkins/jenkins:lts
```

### Run Jenkins with local Dockerfile

```sh
# create image
$ docker build -t ramuspedro/jenkins-with-docker .

# run image
$ docker run --name myjenkins -p 8080:8080 -p 50000:50000 -v jenkins:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock ramuspedro/jenkins-with-docker
```
