FROM teeks99/clang-ubuntu:5

RUN apt-get update && apt-get install -y \
    cmake \
 && rm -rf /var/lib/apt/lists/*

RUN ln /usr/bin/clang-5.0 /usr/bin/clang
