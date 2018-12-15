SHELL=/bin/bash
buildversion=$(shell cat version)
docker_where=cwh
docker_what=wordpress
docker_repo=192.168.1.128:5000

all: build

increment:
	echo $$(( $(buildversion) + 1 )) > version

update: ;
	# placeholder to update code automatically
	#git checkout master && git pull

build: update
	docker build -t $(docker_where)/$(docker_what):$(buildversion) .

latest: build
	docker tag $(docker_where)/$(docker_what):$(buildversion) $(docker_where)/$(docker_what):latest
	docker tag $(docker_where)/$(docker_what):$(buildversion) $(docker_repo)/$(docker_where)/$(docker_what):latest

push: 
	docker push $(docker_repo)/$(docker_where)/$(docker_what):latest
