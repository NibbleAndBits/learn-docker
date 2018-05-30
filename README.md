# Introduction to Docker

## Slides
[PDF](https://github.com/NibbleAndBits/learn-docker/raw/9916f9ffefa0d8d0446f4d56aad5bf13ba785a75/DockerIntro.pdf)

## Swift Language

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

## Kotlin Native

```console
$ docker pull kanfushihara/kotlin-native
```

## Android SDK 

Start a container and open the shell

```console
$ docker run -it thedrhax/android-sdk bash
```

Build the project in current directory

```console
$ docker run -it -v $(pwd):/home/user/project -w /home/user/project -u $(id -u):$(id -g) thedrhax/android-sdk gradle build
```

Persistent Android SDK and caches

-v android-sdk:/home/user/android-sdk-linux

-v gradle-cache:/home/user/.gradle

-v android-cache:/home/user/.android

## References

[Mac Install Docker CE](https://store.docker.com/search?type=edition&offering=community)

[Kitematic](https://kitematic.com/)

[Awesome Docker](https://github.com/veggiemonk/awesome-docker)

[Top Docker Tools](https://stackify.com/top-docker-tools/)

[Docker Hub](https://hub.docker.com/)

[Dockerfile](https://docs.docker.com/engine/reference/builder/)

[Custom Containers](https://github.com/jenkinsci/docker/blob/master/Dockerfile)

[Java Container Example](https://www.jetbrains.com/help/idea/running-a-java-app-in-a-container.html)
