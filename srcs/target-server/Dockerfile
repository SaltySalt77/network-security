FROM nginx:latest

RUN apt update && \
    apt install -y iproute2 iputils-ping iptables snort && \
    apt clean

COPY snort.conf /etc/snort/snort.conf

CMD ["nginx", "-g", "daemon off;"]
