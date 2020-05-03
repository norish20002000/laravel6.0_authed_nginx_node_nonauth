FROM php:7.2-fpm
LABEL maintainer "shudo"

RUN apt-get update \
  && apt-get install -y \
  zlib1g-dev \
  mariadb-client \
  build-essential \
  vim \ 
  git \
  zip \
  unzip \
  && docker-php-ext-install zip pdo_mysql

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

ENV COMPOSER_ALLOW_SUPERUSER 1

ENV COMPOSER_HOME /composer

ENV PATH $PATH:/composer/vendor/bin

RUN composer global require "laravel/installer"

WORKDIR /var/www