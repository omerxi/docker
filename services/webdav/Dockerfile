FROM debian:jessie

RUN apt-get update && apt-get upgrade -q
RUN apt-get install -y apache2 apache2-utils
RUN a2enmod dav
RUN a2enmod dav_fs
RUN service apache2 restart

ADD main.sh .

EXPOSE 6000
