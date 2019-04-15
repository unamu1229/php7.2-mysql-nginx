FROM php:7.2-fpm

# @see https://github.com/dockerdepot/web-containers/issues/10
RUN pecl install xdebug-alpha

COPY ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

RUN curl -sS https://getcomposer.org/installer | php; mv composer.phar /usr/local/bin/composer

RUN apt-get update
RUN apt-get -y upgrade
RUN apt-get install nano less