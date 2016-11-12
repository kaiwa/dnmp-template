FROM php:7-fpm

WORKDIR /var/www

RUN apt-get update && \
    apt-get install -y git

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN docker-php-ext-install \
    pdo_mysql

RUN usermod -u 1000 www-data
