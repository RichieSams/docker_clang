FROM teeks99/clang-ubuntu:6

RUN apt-get update && apt-get install -y \
    cmake \
 && rm -rf /var/lib/apt/lists/*

RUN ln /usr/bin/clang-6.0 /usr/bin/clang
