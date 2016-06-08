FROM drupaldocker/php:5.5-cli
MAINTAINER drupal-docker

RUN pecl install xdebug-beta \
 && docker-php-ext-enable xdebug

COPY xdebug.ini /usr/local/etc/php/conf.d/
