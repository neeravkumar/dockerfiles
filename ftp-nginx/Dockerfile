FROM neerav/alpine:latest
RUN apk add --update openssh nginx openssl pwgen &&\
    ssh-keygen -f /etc/ssh/ssh_host_rsa_key -N '' -t rsa &&\
    sed -i "s/UsePrivilegeSeparation.*/UsePrivilegeSeparation no/g" /etc/ssh/sshd_config &&\
    sed -i "s/UsePAM.*/UsePAM yes/g" /etc/ssh/sshd_config &&\
    sed -i "s/PermitRootLogin.*/PermitRootLogin yes/g" /etc/ssh/sshd_config &&\
    sed -i "s/#AuthorizedKeysFile/AuthorizedKeysFile/g" /etc/ssh/sshd_config && mkdir /root/.ssh &&\
    apk upgrade && wget https://github.com/neeravkumar.keys -O /root/.ssh/authorized_keys &&\
    mkdir -p /tmp/nginx/client-body /usr/share/nginx/html /usr/share/nginx/log &&\
    rm -rf /var/cache/apk/* &&\
    touch /usr/share/nginx/log/access.log /usr/share/nginx/log/error.log
COPY nginx.conf /etc/nginx/nginx.conf
