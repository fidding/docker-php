# This dockerfile uses the php image
# VERSION 1.0
# Author: fidding
FROM php:7.3-fpm

MAINTAINER fidding 395455856@qq.com

# install redis ext
RUN pecl install -o -f redis \
&& rm -rf /tmp/pear \
&& docker-php-ext-enable redis \
&& docker-php-ext-install pdo_mysql

WORKDIR /www
EXPOSE 9000
CMD ["php-fpm"]