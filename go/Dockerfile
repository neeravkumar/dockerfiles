FROM gliderlabs/alpine:edge
RUN mkdir -p /etc/apk && echo "http://alpine.gliderlabs.com/alpine/edge/main" > /etc/apk/repositories &&\
    apk update && apk-install curl git mercurial bzr go && rm -rf /var/cache/apk/*
ENV GOROOT=/usr/lib/go GOPATH=/gopath GOBIN=/gopath/bin PATH=$PATH:$GOROOT/bin:$GOPATH/bin
