# Build development environment

FROM gcc:latest
MAINTAINER yyhclimacool "yyhclimacool@gmail.com"

WORKDIR /root/
ENV IMAGE_BUILT_AT 20191225
RUN touch README.md
RUN echo "## yyhclimacool@gmail.com" > README.md
RUN echo "### image built at : $IMAGE_BUILT_AT" >> README.md

RUN apt update  -y -qq
RUN apt upgrade -y -qq
RUN apt install -y -qq vim
RUN apt install -y -qq tree
RUN apt install -y -qq clang
RUN apt install -y -qq gdb
RUN apt install -y -qq cmake

RUN git config --global credential.helper store
RUN git config --global user.email "yyhclimacool@gmail.com"
RUN git config --global user.name "yyhclimacool"
