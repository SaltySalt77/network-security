FROM kalilinux/kali-rolling

RUN apt update && \
    apt install -y hping3 && \
    apt install -y iputils-ping && \
    apt install -y snort && \
    apt install -y iptables && \
    apt install -y tshark && \
    apt clean

CMD ["sh", "-c", "echo 1 > /proc/sys/net/ipv4/ip_forward && sleep infinity"]
