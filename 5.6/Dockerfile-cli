FROM drupaldocker/php:5.6-cli-2.x
MAINTAINER drupal-docker

RUN apk add --no-cache --virtual .dd-build-deps $PHPIZE_DEPS \
 && pecl install xdebug-2.5.5 \
 && docker-php-ext-enable xdebug \
 && apk del .dd-build-deps

COPY drupal-*.ini /usr/local/etc/php/conf.d/
