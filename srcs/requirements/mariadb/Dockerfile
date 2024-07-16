FROM debian:buster

RUN apt-get update && apt-get install -y mariadb-server mariadb-client

COPY conf/50-server.cnf	/etc/mysql/mariadb.conf.d/50-server.cnf
COPY tools/start.sh /start.sh

EXPOSE 3306

ENTRYPOINT ["sh", "start.sh"]