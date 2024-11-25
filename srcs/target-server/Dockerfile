FROM debian:latest

# 필요한 패키지 설치
RUN apt update && \
    apt install -y iproute2 iputils-ping iptables nginx snort && \
    apt clean

# Snort 설정 파일 복사 (필요시)
COPY snort.conf /etc/snort/snort.conf

# Nginx 설정 파일 복사 (필요시)
COPY nginx.conf /etc/nginx/nginx.conf

# Nginx 로그 디렉토리 생성
RUN mkdir -p /var/log/nginx

# 기본 명령 실행
CMD ["sh", "-c", "echo 1 > /proc/sys/net/ipv4/ip_forward && nginx -g 'daemon off;'"]
