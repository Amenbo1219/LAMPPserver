FROM php:8.0-fpm

# install configure file
RUN cp /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini

# settings
COPY ./php.ini /usr/local/etc/php/conf.d/php.ini

WORKDIR /var/www/html/site/list
