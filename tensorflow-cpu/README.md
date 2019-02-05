## tensorflow-cpu
This repository contains Dockerfile of tensorflow for Docker's automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

### Base Docker Image
This image are based on [tensorflow/tensorflow:1.12.0-py3](https://hub.docker.com/r/tensorflow/tensorflow).
- Ubuntu: 16.04
- Tensorflow: 1.12.0
- Python: 3.5.2
- OpenCV: 3.4.4

### Installation
Install [Docker](https://www.docker.com/) at first, and then download image from [Docker Hub](https://hub.docker.com/).
```sh
$ docker pull watai/tensorflow-cpu
```

### Usage
Start a CPU-only container with Python 3, using the Python interpreter.
```sh
$ docker run -it --rm watai/tensorflow-cpu python
```
Run a Jupyter notebook server with your own notebook directory. To use it, navigate to `http://localhost:8888` or `http://host-ip:8888` in your browser.
```sh
$ docker run -it --rm -p 8888:8888 -v $(realpath ~/notebooks):/notebooks watai/tensorflow-cpu
```
