## tensorflow-gpu
This repository contains Dockerfile of tensorflow-gpu for Docker's automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

### Base Docker Image
This image are based on [tensorflow/tensorflow:1.12.0-gpu-py3](https://hub.docker.com/r/tensorflow/tensorflow).
- Ubuntu: 16.04
- CUDA Toolkit: 9.0
- cuDNN: 7.2.1.38-1+cuda9.0
- Tensorflow-gpu: 1.12.0
- Python: 3.5.2
- OpenCV: 3.4.4

### Installation
Install [Docker](https://www.docker.com/) and [nvidia-docker2](https://github.com/NVIDIA/nvidia-docker) at first, and then download image from [Docker Hub](https://hub.docker.com/).
```sh
$ docker pull watai/tensorflow-gpu
```

### Usage
Start a GPU container with Python 3, using the Python interpreter.
```sh
$ docker run -it --rm --runtime=nvidia watai/tensorflow-gpu python
```
Run a Jupyter notebook server with your own notebook directory. To use it, navigate to `http://localhost:8888` or `http://host-ip:8888` in your browser.
```sh
$ docker run -it --rm --runtime=nvidia -p 8888:8888 -v $(realpath ~/notebooks):/notebooks watai/tensorflow-gpu
```
