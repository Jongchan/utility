# Instruction for docker setup in Ubuntu 14.04 LTS

Tensorflow, Caffe

## Pre-requisite
- install `openssh-client`
- install `nvidia driver` (need to turn off the X-server by `sudo service lightdm stop`.)

## Installation
- [instructions](https://github.com/dgyoo/my-machine-setup/blob/master/nvidia-docker.md) from @dgyoo
  - install docker
  - install nvidia-docker
- pull images from official docker repository ([Tensorflow docker images](https://www.tensorflow.org/versions/r0.11/get_started/os_setup.html#docker-installation))
- Caffe also provides official Docker images, but CUDA 7.5 or higher is required for use. [link](https://github.com/BVLC/caffe)

## Docker command line tools
- Run the docker image to container
  - `sudo nvidia-docker run -it <DOCKER IMAGE NAME> /bin/bash`
- View currently existing containers
  - `sudo docker ps -a`
- Open one container  
  - `sudo nvidia-docker attach <CONTAINER NAME or ID>`
- Start/stop containers  
  - `sudo nvidia-docker start/stop <CONTAINER NAME or ID>`
- Commit (save) the container into new images  
  - `sudo nvidia-docker commit <CONTAINER NAME or ID> <IMAGE NAME:TAG>`
- TODO : how to use private repository for managing images?
