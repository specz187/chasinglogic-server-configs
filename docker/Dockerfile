FROM ubuntu:latest

USER root

ENV GOROOT /usr/local/go
ENV GOPATH /home/cl/go
ENV PATH $PATH:$GOROOT/bin

RUN apt-get update
RUN apt-get upgrade
RUN apt-get install -y curl nginx git mongodb-server

RUN curl -O https://storage.googleapis.com/golang/go1.5.1.linux-amd64.tar.gz
RUN tar -C /usr/local -xzf go1.5.1.linux-amd64.tar.gz
RUN rm go1.5.1.linux-amd64.tar.gz

RUN useradd -m cl -d /home/cl
RUN chown -R cl /home/cl

USER cl

RUN mkdir /home/cl/go
RUN mkdir /home/cl/go/pkg
RUN mkdir /home/cl/go/src
RUN mkdir /home/cl/go/bin


