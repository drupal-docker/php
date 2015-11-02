FROM php:5.5-apache
MAINTAINER zaporylie

RUN apache2ctl -M
RUN a2enmod rewrite
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev
RUN docker-php-ext-install opcache mysqli \
 && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
 && docker-php-ext-install gd
RUN docker-php-ext-install bcmath mbstring
RUN docker-php-ext-install pdo pdo_mysql
