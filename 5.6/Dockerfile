FROM drupaldocker/php:5.6-cli
MAINTAINER drupal-docker

RUN pecl install xdebug-beta \
 && docker-php-ext-enable xdebug

COPY drupal-xdebug.ini /usr/local/etc/php/conf.d/
