projectName = bigdata

build : delete
	docker build -t $(projectName) .

shell : build
	docker run -i -t $(projectName) /bin/bash

run : build
	docker run --name $(projectName) --restart always -d -p 9999:9999 $(projectName) /main.sh

logs :
	docker logs -f $(projectName)

stop :
	-docker stop $(projectName)

delete : stop
	-docker rm $(projectName)

clean : delete
	-docker rmi $(projectName)
