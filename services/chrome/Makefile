projectName = chrome
port = 5000

build :
	docker build -t $(projectName) .

shell : build
	docker run -i -t $(projectName) /bin/bash

clean :
	-docker rmi $(projectName)
