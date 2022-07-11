FROM debian:buster

RUN apt-get -y update && \
	apt-get -y install nginx openssl && \
	mkdir -p /etc/nginx/ssl && \
	openssl req -newkey rsa:2048 -x509 -nodes -days 365\
        -out /etc/nginx/ssl/trurgot.crt \
        -keyout /etc/nginx/ssl/trurgot.key \
        -subj "/C=RU/ST=Moscow/L=Moscow/O=school21/OU=trurgot/CN=https:trurgot.42.fr/emailAddress=trurgot@42.fr"

COPY /conf/nginx.conf /etc/nginx/sites-available/default

EXPOSE 443

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
