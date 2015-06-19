FROM google/debian:wheezy
RUN echo "deb http://http.debian.net/debian wheezy-backports main" >> /etc/apt/sources.list
RUN apt-get update -y && apt-get install --no-install-recommends -y -q curl python build-essential git ca-certificates android-tools-adb
RUN mkdir /nodejs && curl http://nodejs.org/dist/v0.10.33/node-v0.10.33-linux-x64.tar.gz | tar xvzf - -C /nodejs --strip-components=1
ENV PATH $PATH:/nodejs/bin
RUN mkdir omerxi && cd omerxi && git init && git pull https://719a976445b17b79df44d138bf16fbf48c959da9@github.com/omerxi/services.git && cd sms && npm install
ADD main.sh .
EXPOSE 5555
