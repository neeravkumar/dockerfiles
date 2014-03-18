FROM ubuntu:12.04
MAINTAINER me@nero.im
ONBUILD RUN export COUNTRY=$(python -c "import urllib; print urllib.urlopen('http://ipinfo.io/country').read().strip().lower()") && sed -i "s/archive/$COUNTRY.archive/g" /etc/apt/sources.list
ONBUILD RUN apt-get update && apt-get upgrade -y
