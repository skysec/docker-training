FROM ubuntu:14.04

MAINTAINER hecber
# Install server
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -y && apt-get install -y mysql-server
ADD my.cnf /etc/mysql/conf.d/my.cnf 
ADD run.sh /usr/local/bin/run
RUN chmod +x /usr/local/bin/run

VOLUME ["/var/lib/mysql"]
CMD ["/usr/local/bin/run"]
