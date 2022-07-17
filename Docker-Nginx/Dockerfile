FROM alpine:3.13
RUN APK upgrade
RUN APK add nginx
COPY files/default.conf /etc/nginx/httpd.d/default.conf
RUN mkdir -p /var/www/html
WORKDIR /var/www/html
COPY --chown=nginx:nginx /files/html/ .
EXPOSE 80
CMD [ "nginx", "-g", "pid /tmp/nginx.pid; daemon off;" ]
