FROM php:7.0-alpine
MAINTAINER drupal-docker

WORKDIR /var/www/html

RUN apk add --no-cache --virtual .dd-build-deps libpng-dev libjpeg-turbo-dev postgresql-dev libxml2-dev $PHPIZE_DEPS \
  && docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
  && docker-php-ext-install gd mbstring pdo_mysql pdo_pgsql zip \
  && docker-php-ext-install opcache bcmath soap \
  && pecl install redis-3.1.1 \
  && docker-php-ext-enable redis \
  && curl -sS https://getcomposer.org/installer | php \
  && mv composer.phar /usr/local/bin/composer \
  && curl -L -o drush.phar https://github.com/drush-ops/drush-launcher/releases/download/0.4.2/drush.phar \
  && chmod +x drush.phar \
  && mv drush.phar /usr/local/bin/drush \
  && curl -L -o drupal.phar https://drupalconsole.com/installer \
  && chmod +x drupal.phar \
  && mv drupal.phar /usr/local/bin/drupal \
  && echo "export PATH=~/.composer/vendor/bin:\$PATH" >> ~/.bash_profile \
  && apk add --no-cache sudo git libpng libjpeg libpq libxml2 mysql-client openssh-client rsync patch \
  && apk del .dd-build-deps

COPY drupal-*.ini /usr/local/etc/php/conf.d/
COPY cli/drupal-*.ini /usr/local/etc/php/conf.d/
