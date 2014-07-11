FROM ubuntu
MAINTAINER 'Łukasz Jan Niemier'

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y git unzip openssh-server

ADD http://gobuild.io/github.com/gogits/gogs/master/linux/amd64 /tmp/gogs.zip
RUN unzip /tmp/gogs.zip -d /gogs
RUN rm /tmp/gogs.zip
ADD app.ini /gogs/custom/conf/app.ini

VOLUME ["/repositories"]

EXPOSE 80
EXPOSE 22

WORKDIR "/gogs"
ENTRYPOINT ["/gogs/start.sh"]
