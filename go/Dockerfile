FROM gliderlabs/alpine:edge
RUN mkdir -p /etc/apk && echo "http://alpine.gliderlabs.com/alpine/edge/main" > /etc/apk/repositories &&\
    apk update && apk-install curl git mercurial bzr &&\
    curl -LsO https://circle-artifacts.com/gh/andyshinn/alpine-pkg-go/2/artifacts/0/home/ubuntu/alpine-pkg-go/packages/x86_64/go-1.4.2-r0.apk && apk --allow-untrusted add --update go-1.4.2-r0.apk &&\
    rm -rf /var/cache/apk/* && rm -f go-1.4.2-r0.apk
ENV GOROOT=/usr/lib/go GOPATH=/gopath GOBIN=/gopath/bin PATH=$PATH:$GOROOT/bin:$GOPATH/bin
