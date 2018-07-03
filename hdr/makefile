IMG = hdr
INST = hdr1

CONFIG = /home/carltonj2000/cj/configsNscripts
PICS = /home/carltonj2000/cj/cj_pics

CONFIGMAC = /Users/carltonjoseph/cj/configsNscripts
PICSMAC = /Users/carltonjoseph/cj

build:
	docker build -t $(IMG) .

run:
	docker run --name $(INST) -it \
	-v $(CONFIG):$(CONFIG) \
	-v $(PICS):$(PICS) \
	$(IMG) /bin/bash

# need to `rm $(INST)` before running this command
runmac:
	docker run --name $(INST) -it \
	-v $(CONFIGMAC):$(CONFIG) \
	-v $(PICSMAC):$(PICS) \
	$(IMG) /bin/bash

continue:
	docker start -ai $(INST)

clean:
	docker rm -f $(shell docker ps -a | grep $(INST) | cut -b 1-12)

rerun: stopnrun1 run

stopnrun1: stopnrun2 build

stopnrun2: clean
