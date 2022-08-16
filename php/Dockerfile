FROM php:7.4-fpm


# install Drivers
RUN apt-get update && \
  docker-php-ext-install mysqli pdo_mysql

# install configure file
RUN cp /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini

# settings
COPY ./php.ini /usr/local/etc/php/conf.d/php.ini

WORKDIR /var/www/html/site/list
