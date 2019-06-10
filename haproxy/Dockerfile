FROM haproxy:1.7
COPY ./etc/haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg

# Certfication
RUN mkdir /etc/ssl/examplecom/ \
    && chmod -R 400 /etc/ssl/examplecom/
COPY etc/examplecom.pem /etc/ssl/examplecom/examplecom.pem

# HAProxy requires a user & group named haproxy in order to run
RUN groupadd haproxy && useradd -g haproxy haproxy

# HAProxy also requires /var/lib/haproxy/run/haproxy/ to be created before it's run
RUN mkdir -p /var/lib/haproxy/run/haproxy/
