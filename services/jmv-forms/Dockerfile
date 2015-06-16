# SYSTEM
FROM google/debian:wheezy
MAINTAINER Arie Benichou <arie.benichou@gmail.com>
RUN apt-get update && apt-get install -y less nano unzip wget git vim

# JVM
RUN echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu precise main" > /etc/apt/sources.list.d/webupd8team-java.list && \
	apt-key adv --keyserver keyserver.ubuntu.com --recv-keys EEA14886 && \
	echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
	apt-get update && apt-get install -y -q oracle-java8-installer


# SBT
RUN echo "deb http://dl.bintray.com/sbt/debian /" > /etc/apt/sources.list.d/sbt.list
RUN apt-get update && apt-get install -y --force-yes sbt

#RUN mkdir omerxi \
#  && cd omerxi \
#  && git init \
#  && git pull https://ab3d5e570d12ca42efb49fbf8c1a6d10355123c8@github.com/jmvanel/semantic_forms.git \
#  && cd scala/forms_play && sbt dist

RUN git clone git@github.com:jmvanel/semantic_forms.git && cd semantic_forms

#WORKDIR /omerxi/scala/forms_play

#RUN cd /tmp && unzip /omerxi/scala/forms_play/target/universal/semantic_forms_play-1.0-SNAPSHOT.zip

##RUN cd /tmp/semantic_forms_play-1.0-SNAPSHOT/ && sbt "runMain deductions.runtime.sparql_cache.PopulateRDFCache"

#RUN cd /tmp/semantic_forms_play-1.0-SNAPSHOT/ && bin/semantic_forms_play -mem 50 &

#ADD main.sh /

#EXPOSE 9000
