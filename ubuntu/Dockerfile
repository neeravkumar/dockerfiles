FROM ubuntu:14.04
RUN apt-get update && apt-get upgrade -y &&\
    apt-get install openssh-server -y && mkdir /var/run/sshd && echo 'root:root' |chpasswd && sed -ri 's/^PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config && sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config &&\
    echo "service ssh start" > /root/.bashrc && echo "service ssh start" > /.bashrc
CMD /bin/bash
