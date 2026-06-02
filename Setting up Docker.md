1. Log into your Linux Server and Run the following commands

#Uninstall any previous versions docker

for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done

#Download Docker Installation script for Ubuntu

curl -fsSL https://get.docker.com -o get-docker.sh

#Install docker enginge on Ubuntu

sudo sh get-docker.sh

#Verify docker installation

docker version
