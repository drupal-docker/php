FROM php:5.4-cli
MAINTAINER drupal-docker

RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev \
  && rm -rf /var/lib/apt/lists/* \
  && docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
  && docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip

COPY drupal.ini /usr/local/etc/php/conf.d/

WORKDIR /var/www/html
