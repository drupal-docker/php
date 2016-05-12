FROM drupaldocker/php:7.0-fpm
MAINTAINER drupal-docker

RUN pecl install xdebug-beta \
  && docker-php-ext-enable xdebug

COPY xdebug.ini /usr/local/etc/php/conf.d/
