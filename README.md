# docker-repository

## Run 

> git clone https://github.com/13paulmurith/docker-registry.git

> docker-compose up -d

> Access to the web ui : localhost:8081

## Debug

> docker-compose logs

## Configure insecure registries

> nano /lib/systemd/system/docker.service

#### Edit following line

> ExecStart=/usr/bin/dockerd --insecure-registry {registry-ip}:5000

## Pushing local image

> docker image ls

> docker image tag <local-image> <registry-host>:5000/<image-name>:<tag>
  
> docker push docker image tag mthenw/frontail 192.168.1.114/frontail
