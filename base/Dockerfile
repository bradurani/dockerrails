FROM ubuntu
MAINTAINER Brad Urani <bradurani@gmail.com>

RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update -yq
RUN apt-get upgrade -yq
RUN apt-get install -yq wget
RUN apt-get install -yq build-essential
RUN apt-get install -yq libssl-dev
RUN apt-get install -yq openssh-server
RUN apt-get install -yq nano
RUN apt-get install -yq curl
RUN apt-get install -yq less
RUN mkdir /var/run/sshd
RUN echo root:password | chpasswd
CMD /usr/sbin/sshd -D