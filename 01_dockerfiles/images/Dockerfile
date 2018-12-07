FROM ubuntu
MAINTAINER Jamie Dawson (jamierobertdawson@gmail.com)
RUN apt-get update
RUN apt-get install -y nginx
COPY index.html /usr/share/nginx/html/
ENTRYPOINT [“/usr/sbin/nginx”,”-g”,”daemon off;”]
EXPOSE 80
