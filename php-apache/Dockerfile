FROM php:8.1-apache

RUN mkdir -p /var/www/apache-server/html
RUN apt-get update -y && apt-get install -y apache2-utils libaprutil1-dbd-mysql

RUN a2enmod authn_dbd
RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN pecl install redis && docker-php-ext-enable redis
