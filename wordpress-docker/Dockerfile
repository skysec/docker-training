FROM ubuntu:14.04
MAINTAINER Hecber
RUN apt-get -y update && apt-get install -y apache2 \
	php5 \
	php5-mysql \
	php5-gd
VOLUME /var/www/html

COPY wordpress.tgz /usr/local/src/
COPY docker-entrypoint.sh /usr/local/bin/entrypoint.sh

RUN tar -zxf /usr/local/src/wordpress.tgz -C /usr/local/src/ \
#	&& rm /usr/local/src/wordpress.tgz \
	&& chown -R www-data:www-data /var/www/html \
	&& chmod +x /usr/local/bin/entrypoint.sh

ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
CMD ["/usr/sbin/apache2ctl","-D","FOREGROUND"]
LABEL version="0.1"
LABEL tier="frontend"
EXPOSE 80

