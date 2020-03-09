FROM ubuntu:16.04

RUN apt-get update

#RUN apt-get install -y ca-certificates vim mysql-client mysql-server
RUN apt-get install -y ca-certificates vim mysql-client
RUN apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:ondrej/php; exit 0
RUN apt-get update
RUN apt-get install -y --allow-unauthenticated php5.6
RUN apt install -y --allow-unauthenticated libapache2-mod-php5.6 php5.6-mysql
RUN mkdir -p /var/www/rubis
#ADD ./RUBiS/PHP /var/www/rubis/PHP
RUN sed -ie 's/DocumentRoot \/var\/www\/html/DocumentRoot \/var\/www\/rubis/g' /etc/apache2/sites-available/000-default.conf
