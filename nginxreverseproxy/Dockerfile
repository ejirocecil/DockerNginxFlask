FROM nginx:stable-alpine
COPY default.conf /etc/nginx/conf.d
EXPOSE 80/tcp
WORKDIR /usr/share/nginx/html
CMD ["/bin/sh", "-c", "exec nginx -g 'daemon off;';"]
