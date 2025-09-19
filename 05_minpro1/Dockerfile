FROM quay.io/centos/centos:stream9

RUN yum -y -q install vsftpd && yum clean all

VOLUME /var/ftp/pub

COPY vsftpd.conf.template /etc/vsftpd/vsftpd.conf

COPY WelcomeToMyFTPServer.txt /var/ftp/pub

EXPOSE 21 20

ENTRYPOINT [ "/usr/sbin/vsftpd" ]



