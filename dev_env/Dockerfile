# Build development environment

FROM gcc:latest
MAINTAINER yyhclimacool "yyhclimacool@gmail.com"
LABEL maintainer="yyhclimacool@gmail.com"
LABEL version="0.2"
LABEL description="Personl development environment"

WORKDIR /root/
ENV IMAGE_BUILT_AT 20200219

RUN apt update -yqq && apt upgrade -yqq
RUN apt install -yqq vim tree clang gdb cmake

RUN git config --global credential.helper store && \
    git config --global user.email "yyhclimacool@gmail.com" && \
    git config --global user.name "yyhclimacool"

ADD .bashrc .
ADD .vimrc .
#CMD echo "[CMD]Welcome to my dev docker!"
#ENTRYPOINT echo "[ENTRYPOINT]Welcome to my dev docker!"
