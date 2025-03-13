FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl git gcc g++ make

RUN curl -LO https://mafft.cbrc.jp/alignment/software/mafft-7.525-with-extensions-src.tgz && \
    tar -zxvf /root/mafft-7.525-with-extensions-src.tgz && \
    cd /root/mafft-7.525-with-extensions/core/       && make clean && make && make install && \
    cd /root/mafft-7.525-with-extensions/extensions/ && make clean && make && make install

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=mafft
