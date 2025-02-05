FROM nginx:latest
RUN apt-get update && apt-get install -y libnginx-mod-rtmp
COPY nginx.conf /etc/nginx/nginx.conf
