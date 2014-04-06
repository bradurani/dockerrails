FROM bradurani/base
MAINTAINER bradurani@gmail.com
RUN apt-get -y install build-essential zlib1g-dev libssl-dev libreadline6-dev libyaml-dev
RUN wget http://ftp.ruby-lang.org/pub/ruby/2.0/ruby-2.0.0-p247.tar.gz
RUN tar -xvzf ruby-2.0.0-p247.tar.gz
RUN cd ruby-2.0.0-p247 && ./configure --prefix=/usr/local
RUN cd ruby-2.0.0-p247 && make
RUN cd ruby-2.0.0-p247 && make install
CMD /usr/sbin/sshd -D
