FROM debian:stretch

RUN apt-get update && apt-get install -y \
    apt-utils \
    curl \
    build-essential \
    automake \
    autogen \
    bash \
    build-essential \
    bc \
    bzip2 \
    ca-certificates \
    curl \
    file \
    git \
    gzip \
    make \
    ncurses-dev \
    pkg-config \
    libtool \
    python \
    rsync \
    sed \
    bison \
    flex \
    tar \
    vim \
    wget \
    runit \
    xz-utils

RUN echo "deb http://emdebian.org/tools/debian jessie main" > /etc/apt/sources.list.d/emdebian.list
RUN curl http://emdebian.org/tools/debian/emdebian-toolchain-archive.key | apt-key add -
RUN dpkg --add-architecture armel
RUN apt-get update && apt-get install -y crossbuild-essential-armel

# The cross-compiling emulator
RUN apt-get update && apt-get install -y \
    qemu-user \
    qemu-user-static
