FROM ubuntu
MAINTAINER 'Łukasz Jan Niemier'

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y

ADD https://github.com/calmh/syncthing/releases/download/v0.8.11/syncthing-linux-amd64-v0.8.11.tar.gz /tmp/syncthing.tar.gz
