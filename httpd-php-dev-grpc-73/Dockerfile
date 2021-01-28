FROM fpfis/httpd-php-dev:7.3
RUN { \
		echo 'xdebug.mode=debug'; \
		echo 'xdebug.start_with_request=true'; \
	} >> /etc/php/7.3/fpm/php.ini
RUN apt-get update && apt-get install -y telnet autoconf zlib1g-dev php7.3-dev php-pear && rm -rf /var/lib/apt
RUN pecl install grpc
RUN { \
		echo extension=grpc.so \		
	} >> /etc/php/7.3/cli/php.ini
RUN { \
		echo extension=grpc.so \		
	} >> /etc/php/7.3/fpm/php.ini    
