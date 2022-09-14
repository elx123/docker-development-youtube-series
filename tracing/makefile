SHELL := /usr/bin/zsh
VERSION := 1.0
all: playlists-api videos-api videos-api-netcore videos-web
playlists-api:
	docker build \
		-f applications-go/playlists-api/dockerfile \
		-t playlists-api:$(VERSION) \
		--build-arg http_proxy=http://192.168.1.6:7890 \
		--build-arg https_proxy=http://192.168.1.6:7890 \
		.

videos-api:
	docker build \
		-f applications-go/videos-api/dockerfile \
		-t videos-api:$(VERSION) \
		--build-arg http_proxy=http://192.168.1.6:7890 \
		--build-arg https_proxy=http://192.168.1.6:7890 \
		.

videos-api-netcore:
	docker build \
		-f applications-go/videos-api-netcore/dockerfile \
		-t videos-api-netcore:$(VERSION) \
		--build-arg http_proxy=http://192.168.1.6:7890 \
		--build-arg https_proxy=http://192.168.1.6:7890 \
		.

videos-web:
	docker build \
		-f applications-go/videos-web/dockerfile \
		-t videos-web:$(VERSION) \
		--build-arg http_proxy=http://192.168.1.6:7890 \
		--build-arg https_proxy=http://192.168.1.6:7890 \
		.