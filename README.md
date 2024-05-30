# kdc-peru-2024
Repository for KCD - Peru 2024 
This repository was created for the presentation at KCD Lima - Peru 2024

Prerequisites
To use this repository, you need the following installed locally:

- Docker
$ curl https://releases.rancher.com/install-docker/20.10.sh | sh


START
First let's upload the rancher to one of the servers:

$ docker run -d --restart=unless-stopped \
   -v /opt/rancher:/var/lib/rancher \
   -p 80:80 -p 443:443 \
   --privileged \
   rancher/rancher:v2.7.9

