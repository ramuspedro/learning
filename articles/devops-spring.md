# Devops to Spring Projects

Hi! I hope someday I can publish this project somewhere.

This project is based on [Building a spring boot application in jenkins](https://tomgregory.com/building-a-spring-boot-application-in-jenkins/).

This project will provide fundamentals of devops with spring. Enjoy!

## Back-end API

- Spring boot
- Maven package manager

You can test running from intellij or via terminal on _target_ folder

```sh
$ java -jar your-app-0.0.1-SNAPSHOT.jar
```

- Using the API

- GET - http://localhost:8080/api/ride
- POST - http://localhost:8080/api/ride

```json
{
	"name": "Monorail",
	"description": "Sedate ride that takes you around the park.",
	"thrillFactor": 2,
	"vomitFactor": 1
}
```

- GET - http://localhost:8080/api/ride/3

## Docker

The best way to install docker on linux is throught terminal

```sh
$ curl -sSL https://get.docker.com/ | sh
```

## Jenkins

Run Jenkins with docker

```sh
$ docker run --name myjenkins -p 8080:8080 -p 50000:50000 -v jenkins:/var/jenkins_home jenkins/jenkins:lts
```

If it's not configured. Going with default configuration is OK.

Jenkins will be available on http://localhost:8080/. In this case Jenkins is running on the same port of spring service, so e careful.
