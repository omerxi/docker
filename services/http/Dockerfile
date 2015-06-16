FROM google/debian:wheezy
RUN apt-get update -y && apt-get install --no-install-recommends -y -q curl python build-essential git ca-certificates
RUN mkdir /nodejs && curl http://nodejs.org/dist/v0.10.33/node-v0.10.33-linux-x64.tar.gz | tar xvzf - -C /nodejs --strip-components=1
ENV PATH $PATH:/nodejs/bin
RUN mkdir omerxi && cd omerxi && git init && git pull https://719a976445b17b79df44d138bf16fbf48c959da9@github.com/omerxi/omerxi.git && cd nodejs && npm install
ADD main.sh .
WORKDIR /omerxi/nodejs/
EXPOSE 3000
