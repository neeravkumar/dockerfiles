FROM gliderlabs/alpine:edge
RUN mkdir -p /etc/apk && echo "http://alpine.gliderlabs.com/alpine/edge/main" > /etc/apk/repositories &&\
    apk update && apk-install redis &&\
    sed -i 's/daemonize yes/daemonize no/g' /etc/redis.conf &&\
    sed -i 's/# bind 0.0.0.0/bind 0.0.0.0/g' /etc/redis.conf &&\
    rm -rf /var/cache/apk/*
ENTRYPOINT ["/usr/bin/redis-server","/etc/redis.conf"]
EXPOSE 6379
