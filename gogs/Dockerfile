FROM ubuntu
MAINTAINER 'Łukasz Jan Niemier'

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y git-core unzip redis openssh

RUN useradd -d /repositories -m -s /usr/bin/git-shell git

ADD http://gobuild.io/github.com/gogits/gogs/master/linux/amd64 /tmp/gogs.zip
RUN unzip /tmp/gogs.zip -d /gogs
RUN rm /tmp/gogs.zip
RUN mkdir /gogs/config
ADD app.ini /gogs/config/app.ini

VOLUME ["/repositories"]

EXPOSE 80
EXPOSE 22

ENTRYPOINT ["/gogs/start.sh"]
