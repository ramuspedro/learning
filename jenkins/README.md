# Jenkins

## Installation

### Docker

```sh
# Permission on cloud to access a specific folder
$ chown -R 1000:1000 ~/volumes/jenkins

$ docker run --name myjenkins -p 8080:8080 -p 50000:50000 -v ~/volumes/jenkins:/var/jenkins_home jenkins/jenkins:lts
```
