FROM debian:wheezy
MAINTAINER charlie.knudsen@gmail.com

RUN apt-get update && apt-get install -q -y openjdk-7-jdk curl git wget tree unzip

RUN curl -L http://services.gradle.org/distributions/gradle-1.9-bin.zip -o /tmp/gradle-1.9-bin.zip && \
    unzip /tmp/gradle-1.9-bin.zip -d /opt && \
    rm /tmp/gradle-1.9-bin.zip

ENV GRADLE_HOME /opt/gradle-1.9
ENV PATH $GRADLE_HOME/bin:$PATH
