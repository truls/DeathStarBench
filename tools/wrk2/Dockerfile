FROM ubuntu:16.04

COPY . /wrk2

RUN apt-get update \
    && apt-get install -y build-essential luarocks openssl libssl-dev \
    && luarocks install luasocket

RUN cd /wrk2 \
    && make

RUN apt-get remove -y build-essential luarocks libssl-dev \
    && apt-get -y autoremove \
    && apt-get -y clean
