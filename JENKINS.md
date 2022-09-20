# Install using docker

## Basic

```
docker run -p 8080:8080 -p 50000:50000 --restart=on-failure jenkins/jenkins:lts-jdk11
```

## Persist data: volume, name container

```
docker run --name jenkins -d -p 8080:8080 -p 50000:50000 --restart=on-failure -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts-jdk11
```

## References
- [Jenkins Docker Github](https://github.com/jenkinsci/docker/blob/master/README.md)
