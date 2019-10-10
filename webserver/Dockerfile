FROM php:7.2-apache

EXPOSE 80

RUN apt-get update -qy && \
    apt-get install -y

RUN docker-php-ext-install pdo_mysql

COPY apache.conf /etc/apache2/sites-enabled/000-default.conf

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]