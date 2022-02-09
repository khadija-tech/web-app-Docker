FROM python:3.8-slim
RUN apt-get update && apt-get install -y certbot
RUN pip3 install certbot-dns-route53
RUN pip install awscli
RUN mkdir -p /usr/bin/local/scripts
COPY renewcert.sh /usr/bin/local/scripts/
WORKDIR /usr/bin/local/scripts
RUN chmod +x renewcert.sh
RUN ./renewcert.sh
WORKDIR /usr/bin/local/scripts
