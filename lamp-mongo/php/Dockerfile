FROM php:7-apache
COPY php.ini /usr/local/etc/php/
RUN apt-get update \
  && apt-get install -y vim libssl-dev \
  && rm -r /var/lib/apt/lists/* \
  && pecl install mongodb
