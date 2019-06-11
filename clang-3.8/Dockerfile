FROM teeks99/clang-ubuntu:3.8

RUN apt-get update && apt-get install -y \
    cmake \
 && rm -rf /var/lib/apt/lists/*

RUN ln /usr/bin/clang-3.8 /usr/bin/clang
