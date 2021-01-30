FROM php:7.3.18-fpm-alpine

# composer install
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer
RUN docker-php-ext-install pdo_mysql
COPY ./.env /var/www/sample/
WORKDIR /var/www/sample
#COPY composer.json /var/www/sample/
#RUN composer install

RUN apk update

RUN apk add --update nodejs npm

RUN docker-php-ext-install sockets
