FROM php:7.2.19-fpm-alpine3.9
MAINTAINER d9magai
WORKDIR /srv

RUN apk --update --no-cache add \
        icu-dev \
        imap-dev \
        libzip-dev \
        freetype-dev \
    && docker-php-ext-install \
        gd \
        zip \
        imap \
        intl \
        mysqli \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer 

ADD uploads.ini /usr/local/etc/php/conf.d/uploads.ini

