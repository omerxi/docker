# SYSTEM
FROM google/debian:wheezy
MAINTAINER Arie Benichou <arie.benichou@gmail.com>
RUN apt-get update && apt-get install -y less nano unzip wget locate git vi

# JVM
RUN echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu precise main" > /etc/apt/sources.list.d/webupd8team-java.list && \
	apt-key adv --keyserver keyserver.ubuntu.com --recv-keys EEA14886 && \
	echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
	apt-get update && apt-get install -y -q oracle-java8-installer


RUN mkdir omerxi \
  && cd omerxi \
  && git init \
  && git pull https://ab3d5e570d12ca42efb49fbf8c1a6d10355123c8@github.com/jmvanel/semantic_forms.git \
  && cd scala/forms_play && sbt dist

ADD main.sh .

RUN updatedb

EXPOSE 7777
