FROM gliderlabs/alpine:edge
RUN mkdir -p /etc/apk && echo "http://alpine.gliderlabs.com/alpine/edge/main" > /etc/apk/repositories &&\
    apk update && apk-install openjdk7-jre wget &&\
    mkdir -p /rundeck &&\
    cd /rundeck && wget "http://dl.bintray.com/rundeck/rundeck-maven/rundeck-launcher-2.4.2.jar" &&\
    rm -rf /var/cache/apk/*
CMD ["/usr/bin/java","-jar","/rundeck/rundeck-launcher-2.4.2.jar"]
