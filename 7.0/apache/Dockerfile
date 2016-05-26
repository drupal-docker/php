FROM php:7.0-apache
MAINTAINER drupal-docker

VOLUME /var/www/html

ADD https://github.com/phpredis/phpredis/archive/php7.zip /tmp/php7.zip
RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev unzip \
	&& unzip /tmp/php7.zip -d /usr/src/php/ext \
	&& mv /usr/src/php/ext/phpredis-php7 /usr/src/php/ext/redis \
	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip redis \
	&& docker-php-ext-install opcache \
	&& rm -fr /tmp/php7.zip \
	&& apt-get -y purge unzip \
	&& a2enmod rewrite \
	&& rm -rf /var/lib/apt/lists/*

COPY opcache-recommended.ini drupal.ini /usr/local/etc/php/conf.d/

# Add Xdebug.
RUN pecl install xdebug-beta \
  && docker-php-ext-enable xdebug

COPY xdebug.ini /usr/local/etc/php/conf.d/
