FROM php:5.5-cli
MAINTAINER drupal-docker

VOLUME /var/www/html
WORKDIR /var/www/html

RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev sudo git \
  && docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
  && docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip \
  && docker-php-ext-install opcache \
  && pecl install redis \
  && docker-php-ext-enable redis \
  && curl -sS https://getcomposer.org/installer | php \
  && mv composer.phar /usr/local/bin/composer \
  && echo "export PATH=~/.composer/vendor/bin:\$PATH" >> ~/.bash_profile \
  && rm -rf /var/lib/apt/lists/*

COPY opcache-recommended.ini drupal.ini /usr/local/etc/php/conf.d/
