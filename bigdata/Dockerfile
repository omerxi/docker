# SYSTEM
FROM google/debian:wheezy
MAINTAINER Arie Benichou <arie.benichou@gmail.com>
RUN apt-get update && apt-get install -y less nano unzip wget locate

# JVM
RUN echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu precise main" > /etc/apt/sources.list.d/webupd8team-java.list && \
	apt-key adv --keyserver keyserver.ubuntu.com --recv-keys EEA14886 && \
	echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
	apt-get update && apt-get install -y -q oracle-java8-installer

# BIGDATA
#RUN wget http://sourceforge.net/projects/bigdata/files/bigdata/1.5.1/REL.bigdata-1.5.1.tgz/download
#RUN mv download REL.bigdata-1.5.1.tgz
#RUN tar zxvf REL.bigdata-1.5.1.tgz

RUN wget --no-check-certificate https://sourceforge.net/projects/bigdata/files/latest/download -O bigdata-bundled.jar
#RUN mv download bigdata-bundled.jar

ADD main.sh .

RUN updatedb

EXPOSE 9999

