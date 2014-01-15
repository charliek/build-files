# Build file for charliek/gdash
# Not yet working

FROM stackbrew/ubuntu:13.10
MAINTAINER charlie.knudsen@gmail.com

RUN apt-get update
RUN apt-get install -y build-essential git ruby2.0 ruby2.0-dev
RUN git clone git clone https://github.com/ripienaar/gdash.git
RUN cd gdash
RUN gem install bundler
RUN bundle install
