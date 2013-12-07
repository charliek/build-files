# Build file for charliek/oracle-jre-7
# Base image for java apps needing oracle java
# After install java can be found at $JAVA_HOME/bin/java

FROM stackbrew/ubuntu:12.04
MAINTAINER charlie.knudsen@gmail.com

RUN apt-get update && apt-get install -y curl
RUN curl https://charliek-tools.s3.amazonaws.com/jre-7u45-linux-x64.gz -o /opt/jre-7u45-linux-x64.gz
RUN tar zxf /opt/jre-7u45-linux-x64.gz -C /opt && rm /opt/jre-7u45-linux-x64.gz

ENV JAVA_HOME /opt/jre1.7.0_45
