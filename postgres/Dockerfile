FROM gliderlabs/alpine:edge
RUN mkdir -p /etc/apk && echo "http://alpine.gliderlabs.com/alpine/edge/main" > /etc/apk/repositories &&\
    apk update && apk-install postgresql curl &&\
    curl -o /usr/local/bin/gosu -sSL "https://github.com/tianon/gosu/releases/download/1.2/gosu-amd64" &&\
    chmod +x /usr/local/bin/gosu &&\
    curl https://raw.githubusercontent.com/docker-library/postgres/master/docker-entrypoint.sh > /docker-entrypoint.sh
ENV LANG=en_US.utf8 PGDATA=/var/lib/postgresql/data
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["postgres"]
EXPOSE 5432
