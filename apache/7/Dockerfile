FROM php:7-apache
MAINTAINER zaporylie

RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev \
	&& rm -rf /var/lib/apt/lists/* \
	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip

RUN docker-php-ext-install opcache

COPY opcache-recommended.ini /usr/local/etc/php/conf.d/

RUN a2enmod rewrite

# Add drush.
ADD http://files.drush.org/drush.phar /usr/local/bin/drush
RUN php /usr/local/bin/drush core-status -y && chmod a+x /usr/local/bin/drush
RUN drush init -y
