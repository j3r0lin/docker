FROM tutum/apache-php
MAINTAINER jerolin <j3r0lin@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

ADD ./sources.list /etc/apt/sources.list
RUN apt-get update && \
	apt-get -y install \
		php5-mongo \
		php5-dev \
		php5-fpm \
		librabbitmq-dev && \
	apt-get clean && \
	rm -rf /var/lib/apt/lists/* && \
    pecl install amqp && \
	echo "extension=amqp.so" >> /etc/php5/mods-available/amqp.ini && \
	sed -i "s/listen =.*sock/listen = 9000/" /etc/php5/fpm/pool.d/www.conf

EXPOSE 9000
CMD ["php5-fpm", "-F"]
