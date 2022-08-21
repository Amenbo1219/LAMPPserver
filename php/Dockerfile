FROM php:7.4-fpm


# install Drivers
RUN apt-get update && \
  apt-get install -y zlib1g-dev libzip-dev sendmail &&\
  docker-php-ext-install mysqli pdo_mysql zip

# sendemail pathset
RUN echo "sendmail_path=/usr/sbin/sendmail -t -i" >> /usr/local/etc/php/conf.d/sendmail.ini

# install configure file
RUN cp /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini
RUN sed -i '/#!\/bin\/sh/aservice sendmail restart' /usr/local/bin/docker-php-entrypoint
RUN sed -i '/#!\/bin\/sh/aecho "$(hostname -i)\t$(hostname) $(hostname).localhost" >> /etc/hosts' /usr/local/bin/docker-php-entrypoint

# And clean up the image

RUN rm -rf /var/lib/apt/lists/*


# settings
COPY ./php.ini /usr/local/etc/php/conf.d/php.ini



# And clean up the image

RUN rm -rf /var/lib/apt/lists/*


WORKDIR /var/www/html/site/list
