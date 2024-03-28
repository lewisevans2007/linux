# SPDX-License-Identifier: GPL-2.0
#
# extras/Dockerfile
#
# Lewis Evans - January 2024
#
# Docker file for creating a insulated build environment
# for the Linux kernel. This is a Debian based image.

FROM debian:latest

RUN apt-get update
RUN apt-get install -y git \
    fish \
    fakeroot \
    build-essential \
    ncurses-dev \
    xz-utils \
    libssl-dev \
    bc \
    flex \
    libelf-dev \
    bison \
    cpio


RUN apt-get install -y qemu-system-aarch64 vim nano

WORKDIR /linux 

CMD ["/bin/fish"]