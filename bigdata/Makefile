build :
	docker build -t bigdata .

shell : build
	docker run -i -t bigdata /bin/bash

run : build
	docker run -t -p 9999:9999 bigdata /main.sh
