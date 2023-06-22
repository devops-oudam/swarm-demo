FROM debian
WORKDIR /var/www/html
COPY index.html ./
#COPY . .
MAINTAINER oudam
RUN apt update
RUN apt install -y apache2 && apt clean

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
COPY resolv.conf /etc/ 

EXPOSE 80
CMD apachectl -D FOREGROUND

