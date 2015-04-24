FROM ubuntu:trusty
MAINTAINER ademar

RUN apt-get -q update
RUN apt-get -q -y install curl gcc g++ make wget unzip git

COPY build build
CMD ./build

