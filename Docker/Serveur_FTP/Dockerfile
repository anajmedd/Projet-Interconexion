FROM delfer/alpine-ftp-server
RUN apt-get update
RUN apt-get -y install iptables apt-utils iproute2 net-tools systemd telnet nano iputils-ping tcpdump inetutils-traceroute quagga
RUN apt-get -f install
COPY ./quagga /etc/quagga
COPY serveurFTP.sh /home/
RUN ["chmod", "+x", "/home/serveurFTP.sh"]
RUN mkdir /etc/scripts
ENV PATH "/etc/scripts:$PATH"
ENTRYPOINT /etc/init.d/quagga start && /bin/bash
