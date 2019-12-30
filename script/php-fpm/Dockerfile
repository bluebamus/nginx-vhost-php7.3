FROM php:7.3.11-fpm-alpine

RUN apk update && apk upgrade

RUN apk --no-cache add --virtual .build-deps $PHPIZE_DEPS \
  && apk --no-cache add --virtual .ext-deps libmcrypt-dev freetype-dev \
  libjpeg-turbo-dev libpng-dev libxml2-dev msmtp postgresql-dev \
  && docker-php-source extract \
  && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ \
                                   --with-png-dir=/usr/include/ \
                                   --with-jpeg-dir=/usr/include/ \
  && docker-php-ext-install gd pdo pdo_mysql mysqli mbstring  opcache \
  && pecl install xdebug \  
  && docker-php-ext-enable xdebug \
  && docker-php-source delete \
  && apk del .build-deps \
  && docker-php-ext-enable xdebug