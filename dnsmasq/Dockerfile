FROM alpine:edge
RUN mkdir -p /etc/apk && echo "http://alpine.gliderlabs.com/alpine/edge/main" > /etc/apk/repositories &&\
    echo "user=root" >> /etc/dnsmasq.conf &&\
    apk --update add dnsmasq && rm -rf /var/cache/apk/*
CMD ["/usr/sbin/dnsmasq","-k"]
