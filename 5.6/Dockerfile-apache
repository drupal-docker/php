FROM drupaldocker/php:5.6-apache
MAINTAINER drupal-docker

RUN pecl install xdebug-2.5.5 \
 && docker-php-ext-enable xdebug

COPY drupal-*.ini /usr/local/etc/php/conf.d/
