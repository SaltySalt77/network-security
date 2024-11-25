FROM kalilinux/kali-rolling

RUN apt update && \
    apt install -y hping3 && \
    apt install -y iputils-ping && \
    apt install -y snort && \
    apt clean

CMD ["sleep", "infinity"]
