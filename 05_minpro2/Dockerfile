FROM quay.io/centos/centos:9

RUN yum -q -y install httpd php php-fpm php-cli \
    php-common php-mysqlnd php-opcache \
    && yum clean all

ADD src.tar /var/www/html
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

EXPOSE 80

ENTRYPOINT ["/entrypoint.sh"]
