FROM php:8.0-apache

# Here we have created a custom PHP Apache image and an environment that will install mysqli, 
# a PHP extension that will connect the PHP Apache to the MySQL server.
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN apt-get update && apt-get upgrade -y