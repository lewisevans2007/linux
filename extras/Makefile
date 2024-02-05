# SPDX-License-Identifier: GPL-2.0
#
# extras/Makefile
#
# Makefile for the extras directory.
#
# Most of the targets are used to build 
# and run the docker image for testing the kernel
# on environments that are not supported by the
# build system. It also makes it so that the
# entire build is contained within the docker so 
# that if you screw up, you can always restart the container.

DOCKER-ARCH = arm64

build-docker:
	docker build --platform linux/$(DOCKER-ARCH) -t linux-dev extras/.

run-docker:
	sudo docker run -it --privileged --cap-add SYS_ADMIN --cpus=10 --platform linux/arm64 -v .:/linux -v ~/Documents/busybox:/busybox linux-dev
