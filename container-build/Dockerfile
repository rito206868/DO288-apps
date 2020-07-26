# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

RUN sed -i 's/Listen 80/Listen 8080/g' /etc/httpd/conf/httpd.conf && \
    chgrp 0 /var/log/httpd /var/run/httpd && \
    chmod g=u /var/log/httpd /var/run/httpd

LABEL io.openshift.expose-services="8080:http"

EXPOSE 8080

USER 1001


