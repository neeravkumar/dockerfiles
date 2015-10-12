FROM neerav/alpine
RUN echo "http://alpine.gliderlabs.com/alpine/edge/community" >> /etc/apk/repositories &&\
    apk update && apk add dnsmasq sniproxy openssl &&\
    rc-update add dnsmasq default &&\
    rc-update add sniproxy default &&\
    rm /etc/sniproxy/sniproxy.conf &&\
    wget http://raw.githubusercontent.com/ab77/netflix-proxy/master/data/sniproxy.conf -O /etc/sniproxy/sniproxy.conf &&\
    rm -rf /var/cache/apk/*
