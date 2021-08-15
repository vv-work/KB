# Ubuntu

## Docker

### made home assistant work

[Link](https://homeserverworld.com/installing-home-assistant-on-docker/)

```bash 
 docker run -d --name="home-assistant" -v /srv/docker/hassconfig:/config -v /etc/localtime:/etc/localtime:ro -p 8123:8123 homeassistant/home-assistant
```
sudo docker restart gitla

### gitlab 


sudo docker restart gitlab

sudo docker run --detach \
--hostname home-server.com \
--publish 8928:8928 --publish 2289:22 \
--name gitlab \
--restart always \
--volume /srv/gitlab/config:/etc/gitlab \
--volume /srv/gitlab/logs:/var/log/gitlab \
--volume /srv/gitlab/data:/var/opt/gitlab gitlab/gitlab-ce:latest

 docker run -d --name="home-assistant" 
 -v /srv/docker/hassconfig:/config -v 
 /etc/localtime:/etc/localtime:ro -p 8122:8123 homeassistant/home-assistant

gitlab-ctl reconfigure # reconfigure gitlab ecosystem

vim /etc/gitlab/gitlab.rb

sudo docker exec -it gitlab /bin/bash

## Installation on Windows

```ps
#Enable 
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

#Enable Virtual Machine
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

#Download
Invoke-WebRequest -Uri https://wsldownload.azureedge.net/Ubuntu_2004.2020.424.0_x64.appx -OutFile Ubuntu.appx -UseBasicParsing
#Install
Add-AppxPackage .\app_name.appx
```

## Connect

```powershell
ssh coman@home-server
```

## mounting a drive

```bash

sudo lsblk

sudo mount -t ntfs-3g /dev/sdb1 /home/coman/lib
```

bla-bla.

### Plex
sudo docker run \
-d \
--name plex \
-p 32400:32400/tcp \
-p 3005:3005/tcp \
-p 8324:8324/tcp \
-p 32469:32469/tcp \
-p 1900:1900/udp \
-p 32410:32410/udp \
-p 32412:32412/udp \
-p 32413:32413/udp \
-p 32414:32414/udp \
-e TZ="Asia/Jakarta" \
-e PLEX_CLAIM="claim-nNZbyweFzZyjmx8y-63D" \
-e ADVERTISE_IP="193.246.148.58:32400/" \
-v /plex/database:/config \
-v /plex/transcode/temp:/transcode \
-v /plex/media:/data \
--mount type=bind,source=/home/coman/Lib/lib,target=/plex/media \

plexinc/pms-docker

$ docker run -d \
  -it \
  --name devtest \
  --mount type=bind,source=/home/coman/Lib/lib,target=/plex/media \
  nginx:latest