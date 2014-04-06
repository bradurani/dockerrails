FROM bradurani/ruby:2.0.0
RUN gem install rails -v=4.0.0 --no-ri --no-rdoc
RUN apt-get install -yq nodejs
RUN ln -s /usr/bin/node /usr/local/bin/node

#MySql support
RUN apt-get install -yq libmysql-ruby libmysqlclient-dev
RUN apt-get install -yq libqtwebkit-dev

CMD /usr/sbin/sshd -D