FROM ubuntu:23.10

RUN apt-get update && apt-get install -y \
    build-essential git make pkg-config clang \
    g++ g++-mipsel-linux-gnu cpp-mipsel-linux-gnu \
    binutils-mipsel-linux-gnu libcapstone-dev libfreetype-dev \
    libavcodec-dev libavformat-dev libavutil-dev libcurl4-openssl-dev \
    libglfw3-dev libswresample-dev libuv1-dev zlib1g-dev imagemagick

WORKDIR /src/pcsx-redux
RUN git clone --recursive https://github.com/grumpycoders/pcsx-redux.git .
RUN make
RUN make install DESTDIR=/usr/local/pcsx-redux
