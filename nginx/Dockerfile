FROM nginx

LABEL Version=1.0

LABEL Description="This is a nginx image"

LABEL Vendor="Elliott"

RUN adduser elliott

COPY industrious /usr/share/nginx/html

ENV archivo docker

WORKDIR /usr/share/nginx/html

RUN echo "$archivo" > /usr/share/nginx/html/env.html

EXPOSE 90

USER elliott

RUN echo "Yo soy ${whoami}" > /tmp/yo.html

USER root

RUN cp /tmp/yo.html /usr/share/nginx/html/docker.html

VOLUME /var/log/nginx

CMD nginx -g 'daemon off;'