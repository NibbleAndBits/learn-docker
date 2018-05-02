# Introduction to Docker

## Slides
[PDF](https://github.com/NibbleAndBits/learn-docker/blob/master/DockerIntro.pdf)

## Swift Language Images

Start a REPL with latest version default
```console
$ docker run --cap-add sys_ptrace -it --rm --privileged=true swift swift
```

Start a REPL with a version 3.1, 4.0, 4.1... Example shows 4.1.
```console
$ docker run --cap-add sys_ptrace -it --rm --privileged=true swift:4.1 swift
```

Pull the Docker Image From Docker Hub:
```console
$ docker pull swift
```

Create a Container from the Image and Attach It:
```console
$ docker run  -it --name swiftfun swift /bin/bash
```

To Start and Attach Your Image Later:

Start your image with name swiftfun

```console
$ docker start swiftfun
```

and then attach it

```console
$ docker attach swiftfun
```

## References

[Mac Install Docker CE](https://store.docker.com/search?type=edition&offering=community)

[Kitematic](https://kitematic.com/)

[Awesome Docker](https://github.com/veggiemonk/awesome-docker)

[Top Docker Tools](https://stackify.com/top-docker-tools/)

[Docker Hub](https://hub.docker.com/)

[Dockerfile](https://docs.docker.com/engine/reference/builder/)

[Custom Containers](https://github.com/jenkinsci/docker/blob/master/Dockerfile)

[Java Container Example](https://www.jetbrains.com/help/idea/running-a-java-app-in-a-container.html)
