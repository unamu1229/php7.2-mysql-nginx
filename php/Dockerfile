FROM php:7.2-fpm

RUN apt-get update
RUN apt-get install -y wget

# php7.2に対応しているxdebugのリポジトリがなさそうだから、ダウンロードして入れる
# @link https://lowplay.com/articles/install-xdebug-php-72-debian-9
WORKDIR /root
RUN mkdir downloads
RUN wget -O ~/downloads/xdebug-2.6.1.tgz http://xdebug.org/files/xdebug-2.6.1.tgz

WORKDIR downloads
RUN tar -xvzf xdebug-2.6.1.tgz

WORKDIR xdebug-2.6.1
RUN phpize
RUN ./configure
RUN make

RUN mkdir -p /usr/lib/php/20170718
RUN cp modules/xdebug.so /usr/lib/php/20170718/xdebug.so
COPY  ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini