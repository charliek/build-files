FROM debian:wheezy
MAINTAINER charlie.knudsen@gmail.com

RUN apt-get update
RUN apt-get install -y build-essential mercurial git subversion wget
RUN mkdir -p /root/go

ENV HOME /root
ENV GOPATH /root/go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

RUN wget -qO- http://golang.org/dl/go1.3.linux-amd64.tar.gz | tar -C /usr/local -xzf -
