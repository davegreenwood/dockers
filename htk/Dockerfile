FROM i386/ubuntu:16.04

ENV DEBIAN_FRONTEND noninteractive

RUN apt update && apt install -y \
    git \
    build-essential \
    && apt-get clean \
    && rm -rf /tmp/* /var/tmp/* /var/lib/apt/archive/* /var/lib/apt/lists/*

# build from modified source code
RUN git clone -b r3.4.1_fix https://github.com/davegreenwood/HTK.git /htk && \
    cd /htk && \
    ./configure --prefix=/ --disable-hslab &&\
    make all && \
    make install && \
    rm -rf /htk

WORKDIR /ASR
CMD ["bash"]
