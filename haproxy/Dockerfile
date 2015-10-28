FROM ubuntu:14.04
MAINTAINER hecber
RUN apt-get -y update \
	&& apt-get install -y haproxy \
	&& mkdir -p /usr/local/haproxy/etc 

COPY haproxy.conf /usr/local/haproxy/etc/

CMD ["haproxy","-db","-f","/usr/local/haproxy/etc/haproxy.conf"]



