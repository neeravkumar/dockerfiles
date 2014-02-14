FROM ubuntu:12.04
MAINTAINER me@nero.im
RUN apt-get update && apt-get install -y curl
ONBUILD ENV COUNTRY $(curl ipinfo.io/country)
ONBUILD RUN echo deb http://$COUNTRY.archive.ubuntu.com/ubuntu/ precise main universe multiverse > /etc/apt/sources.list && echo deb http://$COUNTRY.archive.ubuntu.com/ubuntu/ precise-security main universe multiverse >> /etc/apt/sources.list
ONBUILD RUN apt-get update && apt-get upgrade
