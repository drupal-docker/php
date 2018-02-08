
FROM alpine:3.7

LABEL maintainer="digitalpulp"

VOLUME /var/www
WORKDIR /var/www

RUN addgroup -g 82 -S www-data \
    && adduser -u 82 -D -S -G www-data www-data

RUN    apk update && \
    apk add \
        php7 \
        php7-bcmath \
        php7-dom \
        php7-ctype \
        php7-curl \
        php7-fileinfo \
        php7-fpm \
        php7-gd \
        php7-iconv \
        php7-intl \
        php7-json \
        php7-mbstring \
        php7-mcrypt \
        php7-mysqlnd \
        php7-opcache \
        php7-openssl \
        php7-pdo \
        php7-pdo_mysql \
        php7-pdo_pgsql \
        php7-pdo_sqlite \
        php7-phar \
        php7-posix \
        php7-simplexml \
        php7-session \
        php7-soap \
        php7-tokenizer \
        php7-xml \
        php7-xmlreader \
        php7-xmlwriter \
        php7-xsl \
        php7-zip \
        php7-zlib \
    && rm -rf /var/cache/apk/* \
    && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    && php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" \
    && php composer-setup.php \
    && php -r "unlink('composer-setup.php');" \
    && mv composer.phar /usr/local/bin/composer \
    && mkdir /sock

COPY magento-*.ini /etc/php7/conf.d/
COPY xdebug.ini /usr/local/etc/php/conf.d/
COPY php-fpm.conf /etc/php7/
COPY www.conf /etc/php7/php-fpm.d

RUN chown -R www-data:www-data /usr/local/etc/php/conf.d /sock

CMD ["php-fpm7", "-F"]
