FROM php:7-fpm
MAINTAINER zaporylie

RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev \
	&& rm -rf /var/lib/apt/lists/* \
	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip

RUN docker-php-ext-install opcache

COPY opcache-recommended.ini /usr/local/etc/php/conf.d/
COPY drupal.ini /usr/local/etc/php/conf.d/
