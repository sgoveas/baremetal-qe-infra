FROM quay.io/centos/centos:stream9

RUN dnf -y update && \
    dnf -y install bind bind-utils iputils procps curl telnet net-tools socat wget && \
    dnf clean all

EXPOSE 53/udp 53/tcp

COPY root/ / 

CMD ["/usr/sbin/named", "-g", "-c", "/etc/named.conf", "-u", "named"]
