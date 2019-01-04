ifndef REGISTRY
REGISTRY := jobteaser
endif

ifndef VERSION
VERSION := alpha
endif

builder:
	@docker build                                          \
	    -t $(REGISTRY)/coretech/pickle/builder:$(VERSION)  \
	    --build-arg git_commit=$(shell git rev-parse HEAD) \
	    --build-arg build_date=$(shell date -u +%FT%TZ)    \
	  .

include build/rules.mk