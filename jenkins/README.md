# Jenkins

## Installation

### Docker

```sh
# Permission on cloud to access a specific folder
$ docker run --name myjenkins -p 8080:8080 -p 50000:50000 -v jenkins:/var/jenkins_home jenkins/jenkins:lts
```
