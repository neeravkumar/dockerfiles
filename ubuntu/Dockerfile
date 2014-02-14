FROM ubuntu:12.04
MAINTAINER me@nero.im
RUN apt-get install -y curl
ONBUILD RUN echo 'deb http://$(curl ipinfo.io/country).archive.ubuntu.com/ubuntu/ precise main universe multiverse' > /etc/apt/sources.list && echo 'deb http://$(curl ipinfo.io/country).archive.ub  untu.com/ubuntu/ precise-security main universe multiverse' >> /etc/apt/sources.list
ONBUILD RUN apt-get update && apt-get upgrade
