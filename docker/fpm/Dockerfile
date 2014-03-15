# Build file for charliek/fpm
# Base image for building fpm packages
# Images can later be run via:
# docker run -i -t charliek/fpm /bin/bash

FROM ubuntu:12.04
MAINTAINER charlie.knudsen@gmail.com

RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y build-essential ruby1.9.1-dev curl
RUN gem install fpm
