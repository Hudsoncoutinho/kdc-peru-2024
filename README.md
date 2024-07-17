# kdc-peru-2024
Repository for KCD - Peru 2024 
This repository was created for the presentation at KCD Lima - Peru 2024

* Acessar servidores 
- sudo ssh -i kcd-lima.pem ubuntu@ IP

- Docker
$ curl https://releases.rancher.com/install-docker/20.10.sh | sh
$ docker ps
" Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: 
Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json": dial unix /var/run/docker.sock: connect: permission denied "

* Resolution:
$ sudo usermod -aG docker $USER
$ newgrp docker
$ groups (find docker)
$ sudo systemctl restart docker

* Cleaning Server:
$ sudo docker system prune --all
$ docker rm -f $(docker ps -a -q)
$ docker volume rm $(docker volume ls)


* Install Rancher Server
$ docker run -d --restart=unless-stopped \
   -v /opt/rancher:/var/lib/rancher \
   -p 80:80 -p 443:443 \
   --privileged \
   rancher/rancher:v2.7.9


* 




