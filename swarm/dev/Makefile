.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/AkashiFeng/s18node/cmd/swarm
	go build -o bin/geth     github.com/AkashiFeng/s18node/cmd/geth
	go build -o bin/bootnode github.com/AkashiFeng/s18node/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/AkashiFeng/s18node/swarm/...
