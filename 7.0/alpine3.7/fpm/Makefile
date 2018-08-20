-include env_make

REPO = anaxexp/base-php
NAME = base-php-$(PHP_VER)

ifeq ($(TAG),)
    ifeq ($(PHP_DEBUG),)
        TAG := $(PHP_VER)
    else
        TAG := $(PHP_VER)-debug
        NAME := $(NAME)-debug
    endif
endif

ifeq ($(BASE_IMAGE_STABILITY_TAG),)
    BASE_IMAGE_TAG := $(ALPINE_VER)
else
    BASE_IMAGE_TAG := $(ALPINE_VER)-$(BASE_IMAGE_STABILITY_TAG)
endif

.PHONY: build test push shell run start stop logs clean release

default: build

build:
	docker build -t $(REPO):$(TAG) \
		-f Dockerfile.anaxexp \
		--build-arg PHP_DEBUG=$(PHP_DEBUG) \
		--build-arg BASE_IMAGE_TAG=$(BASE_IMAGE_TAG) ./

test:
	IMAGE=$(REPO):$(TAG) ./test.sh

push:
	docker push $(REPO):$(TAG)

shell:
	docker run --rm --name $(NAME) -i -t $(PORTS) $(VOLUMES) $(ENV) $(REPO):$(TAG) /bin/bash

run:
	docker run --rm --name $(NAME) $(PORTS) $(VOLUMES) $(ENV) $(REPO):$(TAG) $(CMD)

start:
	docker run -d --name $(NAME) $(PORTS) $(VOLUMES) $(ENV) $(REPO):$(TAG)

stop:
	docker stop $(NAME)

logs:
	docker logs $(NAME)

clean:
	-docker rm -f $(NAME)

release: build push
