FROM ubuntu

ENV DEBIAN_FRONTEND=noninteractive


RUN apt-get update -y && apt-get install -y nginx
CMD ["ls"]
EXPOSE 8080

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
