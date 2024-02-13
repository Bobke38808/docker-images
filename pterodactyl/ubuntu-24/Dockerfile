FROM ubuntu:24.04

MAINTAINER bbk

RUN apt-get update -y && \
    apt-get install adduser -y && \
    adduser --disabled-password --home /home/container container

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
