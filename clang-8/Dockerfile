FROM quay.io/richiesams/ubuntu:bionic

ARG llvmver=8

RUN apt-get update && apt-get install -y \
    # Install pre-reqs
    ca-certificates \
    build-essential \
    # Install Tools
    clang-$llvmver \
    lldb-$llvmver \
    lld-$llvmver \
    libc++-dev \
    libc++abi-dev \
    valgrind \
 && rm -rf /var/lib/apt/lists/*

RUN ln /usr/bin/clang-$llvmver /usr/bin/clang
RUN ln /usr/bin/clang++-$llvmver /usr/bin/clang++

ADD https://github.com/Kitware/CMake/releases/download/v3.16.4/cmake-3.16.4-Linux-x86_64.sh /cmake-3.16.4-Linux-x86_64.sh
RUN mkdir /opt/cmake \
    && sh /cmake-3.16.4-Linux-x86_64.sh --prefix=/opt/cmake --skip-license \
    && ln -s /opt/cmake/bin/cmake /usr/local/bin/cmake \
    && rm /cmake-3.16.4-Linux-x86_64.sh
