FROM robcherry/docker-chromedriver
RUN apt-get update -y && apt-get install git
RUN mkdir /nodejs && curl http://nodejs.org/dist/v0.10.33/node-v0.10.33-linux-x64.tar.gz | tar xvzf - -C /nodejs --strip-components=1
ENV PATH $PATH:/nodejs/bin
RUN mkdir omerxi && cd omerxi && git init && git pull https://ab3d5e570d12ca42efb49fbf8c1a6d10355123c8@github.com/omerxi/semantize.git && cd vtc/phones && npm install
ADD main.sh .
EXPOSE 6000
