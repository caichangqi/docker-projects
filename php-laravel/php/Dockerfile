FROM php:7-apache
COPY php.ini /usr/local/etc/php/
RUN apt-get update \
  && apt-get install -y vim libssl-dev libmcrypt-dev libicu-dev \
  && rm -r /var/lib/apt/lists/* \
  && pecl install mongodb \
  && docker-php-ext-install pdo_mysql mysqli \
     mbstring mcrypt

# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer

# Put apache config for Laravel
COPY laravel.conf /etc/apache2/sites-available/laravel.conf
RUN a2dissite 000-default.conf && a2ensite laravel.conf && a2enmod rewrite

WORKDIR /var/www/html