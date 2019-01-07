Readme for Simplify LAMP Stack Development with Docker - developering-lamp-stack-docker

https://anthonychu.ca/post/developing-lamp-stack-docker/
docker run -d -p 8080:80 -v /Users/puj/docker/developing-lamp-stack-docker/www:/var/www/html php:apache

Deploy a ready-to-use, consistent lemp stack, anywhere with Docker
https://medium.com/@bulgr0z/deploy-a-ready-to-use-consistent-lamp-stack-anywhere-with-docker-eaf669283f31
All in dockerfiles

Run mysql:
docker run -d -v /Users/puj/docker/dockerfiles/mysql-data:/var/lib/mysql --name mysql bulgroz/mysql && docker logs -f mysql
=========================================================================
#  Creating admin account...
=========================================================================
#
#  YOUR MYSQL CREDENTIALS
#    login: admin
#    password: Pt?84LKm78KF
#========================================================================


$ docker run -d -p <your public ip>:80:80 \
-v /home/nginx-sites/sites-enabled/:/etc/nginx/sites-enabled \
-v /home/nginx-sites/sites-available/:/etc/nginx/sites-available \
-v /home/nginx-sites/logs/:/var/log/nginx \
-v /home/www/:/home/www \
--name nginx \
--link mysql:mysql bulgroz/nginxphp

$ docker run -d -p 127.0.0.1:80:80 \
-v /Users/puj/docker/dockerfiles/nginx-sites/sites-enabled/:/etc/nginx/sites-enabled \
-v /Users/puj/docker/dockerfiles/nginx-sites/sites-available/:/etc/nginx/sites-available \
-v /Users/puj/docker/dockerfiles/nginx-sites/logs/:/var/log/nginx \
-v /Users/puj/docker/dockerfiles/www/:/home/www \
--name nginx \
--link mysql:mysql bulgroz/nginxphp

docker run -d -p 8080:80 \
-v /Users/puj/docker/dockerfiles/nginx-sites/sites-enabled/:/etc/nginx/sites-enabled \
-v /Users/puj/docker/dockerfiles/nginx-sites/sites-available/:/etc/nginx/sites-available \
-v /Users/puj/docker/dockerfiles/nginx-sites/logs/:/var/log/nginx \
-v /Users/puj/docker/dockerfiles/www/:/home/www \
--name nginx \
--link mysql:mysql bulgroz/nginxphp