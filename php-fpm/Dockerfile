FROM php:7.0.9-fpm-alpine

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install -j$(grep -c ^processor /proc/cpuinfo 2>/dev/null || 1) iconv gd mbstring fileinfo curl spl ftp json zip calendar

VOLUME /var/www/html