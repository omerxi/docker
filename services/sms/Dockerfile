FROM google/debian:wheezy
RUN apt-get update -y && apt-get install --no-install-recommends -y -q curl python build-essential git ca-certificates
RUN mkdir /nodejs && curl http://nodejs.org/dist/v0.10.33/node-v0.10.33-linux-x64.tar.gz | tar xvzf - -C /nodejs --strip-components=1
ENV PATH $PATH:/nodejs/bin
RUN mkdir omerxi && cd omerxi && git init && git pull https://ab3d5e570d12ca42efb49fbf8c1a6d10355123c8@github.com/omerxi/services.git && cd sms && npm install
ADD main.sh .
EXPOSE 3000
