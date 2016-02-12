FROM php:7-apache
MAINTAINER zaporylie

RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev git \
	&& rm -rf /var/lib/apt/lists/* \
	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip

RUN docker-php-ext-install opcache

COPY opcache-recommended.ini /usr/local/etc/php/conf.d/

RUN curl -sS https://getcomposer.org/installer | php \
  && mv composer.phar /usr/local/bin/composer \
  && composer global require drush/drush:dev-master

RUN pecl install xdebug-beta \
  && docker-php-ext-enable xdebug

RUN a2enmod rewrite
