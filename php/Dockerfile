FROM php:8.1-fpm-alpine

# Install Postgres PDO
RUN set -ex \
  && apk --no-cache add \
  postgresql-dev

RUN docker-php-ext-install pdo pdo_mysql pgsql pdo_pgsql

# COPY LOCAL PHP INI FILE TO CONTAINER...
COPY ./php/config/php.ini /usr/local/etc/php
