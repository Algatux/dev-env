FROM nginx:1.13.1

MAINTAINER Alessandro Galli <a.galli85@gmail.com>

COPY config/host.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
