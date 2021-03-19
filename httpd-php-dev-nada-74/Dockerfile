FROM fpfis/httpd-php-dev:7.4

RUN sudo apt-key adv --refresh-keys --keyserver keyserver.ubuntu.com
RUN apt-get update && apt-get -y install wget zip git telnet autoconf zlib1g-dev php7.4-dev php-pear
RUN pecl install mongodb

RUN { \
		echo 'extension=mongodb.so'; \		
        echo 'date.timezone = "america/new_york"'; \
	} >> /etc/php/7.4/cli/php.ini
RUN { \
		echo 'extension=mongodb.so'; \		
        echo 'date.timezone = "america/new_york"'; \
	} >> /etc/php/7.4/fpm/php.ini  

RUN apt install -y libxslt-dev && rm -rf /var/lib/apt
