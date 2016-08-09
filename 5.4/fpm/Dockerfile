FROM drupaldocker/php:5.4-fpm
MAINTAINER drupal-docker

RUN pecl install xdebug-beta \
 && docker-php-ext-enable xdebug

COPY drupal-*.ini /usr/local/etc/php/conf.d/
