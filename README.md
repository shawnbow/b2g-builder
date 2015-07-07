This image is created to help B2G developers especially for Matchstick developers to setup a docker build environment, for more stuffs about Matchstick, please refer to [Matchstick.tv](http://www.matchstick.tv/). 

####Features:
* ubuntu:14.04
* Firefox OS build required packages
* NodeJS 0.12.6
* OpenSSHServer

####Usage:
* docker run -d -p 2222:22 -v $work-dir:$work-dir shawnbow/b2g-builder
* 'ssh root@127.0.0.1 -p 2222', the password is 'root'.
* For the first time login as root user, I strongly suggest to run 'useradd -u $(stat -c %u $work-dir) -s /bin/bash -m build' to create a default build user which has the same access permission with your host shared volume, since I don't think you would like to see your source code is messed up after building with root user. 
* 'cd $work-dir && su build'
* Get into your b2g project path, run './build.sh'
* Screen manager is also added into the image, you can build your project with screen. 

####References:
* [simonjohansson/b2g-build](https://registry.hub.docker.com/u/simonjohansson/b2g-build/)
* [rastasheep/ubuntu-sshd](https://registry.hub.docker.com/u/rastasheep/ubuntu-sshd/)
* [google/nodejs](https://registry.hub.docker.com/u/google/nodejs/)
