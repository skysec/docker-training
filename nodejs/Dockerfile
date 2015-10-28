FROM ubuntu:14.04
MAINTAINER hecber
RUN apt-get update -y \
	&& apt-get install -y npm

COPY blog /usr/local/src/blog

RUN cd /usr/local/src/blog \
	&& npm install

EXPOSE 8080

CMD ["nodejs","/usr/local/src/blog/app.js"]

