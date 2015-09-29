FROM ubuntu:latest

USER root

ENV GOROOT /usr/local/go
ENV GOPATH /go
ENV PATH $PATH:$GOROOT/bin

RUN mkdir /go
RUN mkdir /go/pkg
RUN mkdir /go/src
RUN mkdir /go/bin

RUN apt-get install -y curl nginx

RUN curl -O https://storage.googleapis.com/golang/go1.5.1.linux-amd64.tar.gz
RUN tar -C /usr/local -xzf go1.5.1.linux-amd64.tar.gz
RUN rm go1.5.1.linux-amd64.tar.gz
