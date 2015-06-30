projectName = http
port = 3000

build :
	docker build -t $(projectName) .

shell : build
	docker run -i -t $(projectName) /bin/bash

run : delete build
	docker run \
	--name $(projectName) \
	--restart always \
	-d \
	-p 80:$(port) \
	-v /etc/localtime:/etc/localtime:ro \
	$(projectName) \
	/main.sh

logs :
	docker logs -f $(projectName)

stop :
	-docker stop $(projectName)

delete : stop
	-docker rm $(projectName)

clean : delete
	-docker rmi $(projectName)
