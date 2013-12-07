# Build file for charliek/java7
# Base image for java apps

FROM stackbrew/ubuntu:13.04
MAINTAINER charlie.knudsen@gmail.com

RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install openjdk-7-jre-headless curl
RUN echo "JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64/" >> /etc/environment

 