FROM nginx:1.20

RUN apt-get update

RUN apt-get install -y nano

COPY ./conf.d /etc/nginx/conf.d

WORKDIR /var/www

EXPOSE 80