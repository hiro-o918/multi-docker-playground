PWD := $(shell pwd)
IMAGE_NAME := k8s-complex-nginx
VTAG := latest

.PHONY: dev/build
dev/build:
	docker build \
		-t hiro918/dev-$(IMAGE_NAME):$(VTAG) \
		-f Dockerfile.dev \
		$(PWD)

.PHONY: dev/run
dev/run:
	docker run \
		hiro918/dev-$(IMAGE_NAME):$(VTAG)

.PHONY: build
build:
	docker build \
		-t hiro918/$(IMAGE_NAME):$(VTAG) \
		-f Dockerfile\
		$(PWD)

.PHONY: run
run:
	docker run \
		-it \
		hiro918/$(IMAGE_NAME):$(VTAG)
