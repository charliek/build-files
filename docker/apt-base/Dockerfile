FROM debian:wheezy
MAINTAINER charlie.knudsen@gmail.com

RUN apt-get update && apt-get install -q -y wget

RUN wget -qO - http://charliek-apt.s3-website-us-west-2.amazonaws.com/dists/pubkey.gpg | apt-key add -
RUN echo "deb http://charliek-apt.s3-website-us-west-2.amazonaws.com trusty prod" > /etc/apt/sources.list.d/charliek.list
ONBUILD RUN sudo apt-get update
