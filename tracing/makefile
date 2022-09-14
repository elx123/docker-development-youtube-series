SHELL := /usr/bin/zsh
VERSION := 1.0
all: playlists-api videos-api videos-api-netcore videos-web
playlists-api:
	docker build \
		-f playlists-api \
		-t playlists-api:$(VERSION) \
		--build-arg BUILD_REF=$(VERSION) \
		--build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` \
		.

videos-api:
	docker build \
		-f videos-api \
		-t videos-api:$(VERSION) \
		--build-arg BUILD_REF=$(VERSION) \
		--build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` \
		.

videos-api-netcore:
	docker build \
		-f videos-api-netcore \
		-t videos-api-netcore:$(VERSION) \
		--build-arg BUILD_REF=$(VERSION) \
		--build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` \
		.

videos-web:
	docker build \
		-f videos-web \
		-t videos-web:$(VERSION) \
		--build-arg BUILD_REF=$(VERSION) \
		--build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` \
		.