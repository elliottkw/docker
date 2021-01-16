FROM centos:7

LABEL Version=1.0

LABEL Description="This is an apache image"

LABEL Vendor=Elliott

RUN yum install -y httpd

COPY bislite /var/www/html/

RUN echo "$(whoami)" > /var/www/html/user1.html

RUN adduser elliott

USER elliott

RUN echo "$(whoami)" > /tmp/user2.html

USER root

RUN cp /tmp/user2.html /var/www/html/user2.html

COPY run.sh /run.sh

CMD sh /run.sh