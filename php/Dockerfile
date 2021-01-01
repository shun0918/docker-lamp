FROM php:8.0-apache
LABEL maintainer shunnihei

COPY ./php.ini /usr/local/etc/php
COPY ./apache2.conf /etc/apache2/conf-enabled

RUN apt-get update \
    && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev libmcrypt-dev vim \
    && docker-php-ext-install mysqli pdo_mysql gd

RUN a2enmod rewrite