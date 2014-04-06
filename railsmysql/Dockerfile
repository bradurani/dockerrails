FROM bradurani/rails:4.0.0
RUN apt-get install -y -q mysql-client mysql-server

RUN sed -i -e"s/^bind-address\s*=\s*127.0.0.1/bind-address = 0.0.0.0/" /etc/mysql/my.cnf

RUN /usr/sbin/mysqld & \
    sleep 10s &&\
    echo "GRANT ALL ON *.* TO root@'%' IDENTIFIED BY '' WITH GRANT OPTION; FLUSH PRIVILEGES" | mysql
EXPOSE 3306
RUN apt-get install -y -q libmysql-ruby libmysqlclient-dev
RUN apt-get install -y -q libqtwebkit-dev
CMD ["/usr/bin/mysqld_safe"]