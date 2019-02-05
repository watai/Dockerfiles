## Dockerfiles
This repository contains Dockerfiles for Docker's automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

### Build Image
```sh
# Build image
$ docker build -f ~/Dockerfile -t {ImageName} .
```

### Run container
```sh
# CPU-based images
$ docker run -it --rm {ImageName} bash
# GPU-based images (set up nvidia-docker2 first)
$ docker run -it --rm --runtime=nvidia {ImageName} bash
```
