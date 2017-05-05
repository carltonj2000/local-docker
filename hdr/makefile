IMG = hdr
INST = hdr1

CONFIG = /home/carltonj2000/cj/configsNscripts
PICS = /home/carltonj2000/cj/cj_pics

build:
	docker build -t $(IMG) .

run:
	docker run --name $(INST) -it \
	-v $(CONFIG):$(CONFIG) \
	-v $(PICS):$(PICS) \
	$(IMG) /bin/bash

clean:
	docker rm -f $(shell docker ps -a | grep $(INST) | cut -b 1-12)

rerun: stopnrun1 run

stopnrun1: stopnrun2 build

stopnrun2: clean
