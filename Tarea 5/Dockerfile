FROM nginx
MAINTAINER María Jesús Alloza Rodríguez "mariajesus.allozarodriguez@gmail.com"
RUN apt-get update && apt-get upgrade -y && apt-get install mariadb-client -y && apt-get clean && rm -rf /var/lib/apt/lists/*
ADD bookmedik /usr/share/nginx/html
ADD script.sh /opt/
RUN chmod +x /opt/script.sh && rm /usr/share/nginx/html/index.html
ENTRYPOINT ["/opt/script.sh"]
