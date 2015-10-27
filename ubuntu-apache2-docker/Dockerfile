FROM ubuntu:14.04
MAINTAINER Hecber
RUN apt-get -y update && apt-get install -y apache2
CMD ["/usr/sbin/apache2ctl","-D","FOREGROUND"]
LABEL version="0.1"
LABEL tier="frontend"
EXPOSE 80

