FROM drupaldocker/php:7.0-cli
MAINTAINER drupal-docker

RUN pecl install xdebug-beta \
 && docker-php-ext-enable xdebug

COPY drupal-xdebug.ini /usr/local/etc/php/conf.d/
