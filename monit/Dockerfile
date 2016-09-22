FROM neerav/alpine
RUN apk update && apk add monit && apk clean &&\
    rc-update add monit default &&\
    sed -i 's/use address localhost/# use address localhost/g' /etc/monitrc &&\
    sed -i 's/allow localhost/# allow localhost/g' /etc/monitrc &&\
    rm -rf /var/cache/apk/*
