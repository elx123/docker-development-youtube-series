SHELL := /usr/bin/zsh
PROXY := http://192.168.1.6:7890
VERSION := 1.0
all: playlists-api videos-api videos-api-netcore videos-web
playlists-api:
	docker build \
		-f applications-go/playlists-api/dockerfile \
		-t playlists-api:$(VERSION) \
		--build-arg http_proxy=$(PROXY) \
		--build-arg https_proxy=$(PROXY) \
		.

videos-api:
	docker build \
		-f applications-go/videos-api/dockerfile \
		-t videos-api:$(VERSION) \
		--build-arg http_proxy=$(PROXY) \
		--build-arg https_proxy=$(PROXY) \
		.

videos-api-netcore:
	docker build \
		-f applications-go/videos-api-netcore/dockerfile \
		-t videos-api-netcore:$(VERSION) \
		--build-arg http_proxy=$(PROXY) \
		--build-arg https_proxy=$(PROXY) \
		.

videos-web:
	docker build \
		-f applications-go/videos-web/dockerfile \
		-t videos-web:$(VERSION) \
		--build-arg http_proxy=$(PROXY) \
		--build-arg https_proxy=$(PROXY) \
		.

aliyuncs-upload:
	docker tag playlists-api:$(VERSION) registry.cn-shanghai.aliyuncs.com/testcjj/playlists-api:$(VERSION)
	docker tag videos-api:$(VERSION) registry.cn-shanghai.aliyuncs.com/testcjj/videos-api:$(VERSION)
	docker tag videos-web:$(VERSION) registry.cn-shanghai.aliyuncs.com/testcjj/videos-web:$(VERSION)
	docker push registry.cn-shanghai.aliyuncs.com/testcjj/playlists-api:$(VERSION)
	docker push registry.cn-shanghai.aliyuncs.com/testcjj/videos-api:$(VERSION)
	docker push registry.cn-shanghai.aliyuncs.com/testcjj/videos-web:$(VERSION)