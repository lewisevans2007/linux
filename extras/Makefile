# SPDX-License-Identifier: GPL-2.0
#
# extras/Makefile
#
# Makefile for the extras directory. Ignored by main Makefile.

DOCKER-ARCH = arm64

build-docker:
	docker build --platform linux/$(DOCKER-ARCH) -t linux-dev extras/.

run-docker:
	sudo docker run -it --privileged --cap-add SYS_ADMIN --cpus=10 --platform linux/arm64 -v .:/linux -v ~/Documents/busybox:/busybox linux-dev
