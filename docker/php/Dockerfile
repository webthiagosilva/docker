FROM php:7.4-fpm

ARG user
ARG uid

RUN apt-get -y update && apt-get -y update

RUN apt-get install -y nano

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN useradd -G www-data,root -u $uid -d /home/$user $user
RUN mkdir -p /home/$user/.composer && \
    chown -R $user:$user /home/$user


#COPY ./conf.d/php.ini /usr/local/etc/php/php.ini
#COPY ./conf.d/www.conf /usr/local/etc/php-fpm.d/www.conf

EXPOSE 9000

WORKDIR /var/www