FROM neerav/alpine:latest
RUN echo "http://alpine.gliderlabs.com/alpine/edge/testing" >> /etc/apk/repositories &&\
    apk add --update consul &&\
    rc-update add consul default &&\
    rc-update add syslog default &&\
    rm -rf /var/cache/apk/*
