FROM php:8.0-apache


# Here we have created a custom PHP Apache image and an environment that will install mysqli, 
# a PHP extension that will connect the PHP Apache to the MySQL server.
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN apt-get update && apt-get upgrade -y


# Get latest Composer, composer is copied from the Docker hub...? Left side is the Docker hub, right side pc?
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

COPY docker/xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini