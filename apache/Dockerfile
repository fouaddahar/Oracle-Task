FROM oraclelinux
MAINTAINER Fouad DAHAR
USER root

ENV HTTPD_VERSION=2.4

#Update image
RUN yum -y install httpd \
    && yum install -y git \
    && cd /var/www/html/ \
    && git clone https://github.com/igameproject/Breakout.git \
    && cp -rf /var/www/html/Breakout/* /var/www/html/ \
    && rm -rf /var/www/html/Breakout/ \
    && sed -i '/Listen [0-9]*/s//Listen 8080/' /etc/httpd/conf/httpd.conf

EXPOSE 8080

ENTRYPOINT /usr/sbin/httpd -D FOREGROUND
