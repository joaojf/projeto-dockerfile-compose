FROM nginx:latest

ENV app_dir /usr/share/nginx/html/
WORKDIR ${app_dir}
COPY cep.html ${app_dir}

LABEL description="Webserver"
LABEL versio="1.0.0"

EXPOSE 80/tcp
ENTRYPOINT ["/usr/sbin/nginx"]
CMD ["-g", "daemon off;"]
