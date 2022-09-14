SHELL := /usr/bin/zsh
VERSION := 1.0
all: playlists-api videos-api videos-api-netcore videos-web
playlists-api:
	docker build \
		-f applications-go/playlists-api/dockerfile \
		-t playlists-api:$(VERSION) \
		--build-arg BUILD_REF=$(VERSION) \
		--build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` \
		.

videos-api:
	docker build \
		-f applications-go/videos-api/dockerfile \
		-t videos-api:$(VERSION) \
		--build-arg BUILD_REF=$(VERSION) \
		--build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` \
		.

videos-api-netcore:
	docker build \
		-f applications-go/videos-api-netcore/dockerfile \
		-t videos-api-netcore:$(VERSION) \
		--build-arg BUILD_REF=$(VERSION) \
		--build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` \
		.

videos-web:
	docker build \
		-f applications-go/videos-web/dockerfile \
		-t videos-web:$(VERSION) \
		--build-arg BUILD_REF=$(VERSION) \
		--build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` \
		.