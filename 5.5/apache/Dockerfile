FROM drupaldocker/php:5.5-apache
MAINTAINER drupal-docker

RUN pecl install xdebug-beta \
 && docker-php-ext-enable xdebug

COPY drupal-*.ini /usr/local/etc/php/conf.d/
