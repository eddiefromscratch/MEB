FROM debian:stable-slim

RUN apt-get update && apt-get install -y gcc make gengetopt g++ libx11-dev

COPY sgframework /tmp/src

ENV DEST_DIR=/usr/local/bin
RUN cd /tmp/src && make clean && make config && make && make install && cd ../ && rm -rf /tmp/src
