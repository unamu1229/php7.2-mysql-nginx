FROM php:7.2-fpm

# @see https://github.com/dockerdepot/web-containers/issues/10
RUN pecl install xdebug-alpha

COPY  ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini