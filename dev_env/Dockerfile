# Build development environment

FROM gcc:latest
MAINTAINER yyhclimacool "yyhclimacool@gmail.com"
LABEL maintainer="yyhclimacool@gmail.com"
LABEL version="0.2"
LABEL description="Personl development environment"

WORKDIR /root/
ENV IMAGE_BUILT_AT 20200219
ENV LD_LIBRARY_PATH /lib:/lib64:/usr/lib:/usr/lib64:/usr/local/lib:/usr/local/lib64

RUN ln -s /usr/local/bin/gfortran /usr/bin/gfortran
RUN apt update -yqq && apt upgrade -yqq
RUN apt install -yq vim tree clang gdb cmake \
    automake bison flex libboost-all-dev libevent-dev \
    libssl-dev libtool make pkg-config python2-dev python3-dev

RUN git config --global credential.helper store && \
    git config --global user.email "yyhclimacool@gmail.com" && \
    git config --global user.name "yyhclimacool"

ADD .bashrc .
ADD .vimrc .
#CMD echo "[CMD]Welcome to my dev docker!"
#ENTRYPOINT echo "[ENTRYPOINT]Welcome to my dev docker!"
