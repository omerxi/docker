FROM google/debian:wheezy
MAINTAINER Arie Benichou <arie.benichou@gmail.com>

RUN apt-get update && apt-get install wget -y
RUN wget http://sourceforge.net/projects/bigdata/files/bigdata/1.5.1/REL.bigdata-1.5.1.tgz/download
RUN mv download REL.bigdata-1.5.1.tgz
RUN tar zxvf REL.bigdata-1.5.1.tgz

