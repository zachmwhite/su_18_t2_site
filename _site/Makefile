REMOTEUSER ?= zmw5
REMOTEHOST ?= cabbage.stat.duke.edu
REMOTEDIR ?= /web/isds/docs/courses/Summer18/sta104.001-1
REMOTE ?= $(REMOTEUSER)@$(REMOTEHOST):$(REMOTEDIR)

.PHONY: clean
clean:
	rm -rf _site/*

push: build
	rsync -az _site/* $(REMOTE)


build:
	jekyll build

serve:
	jekyll serve --watch --baseurl ''