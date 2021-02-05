FROM fpfis/httpd-php-dev:7.3
RUN { \
		echo 'xdebug.mode=debug'; \
		echo 'xdebug.start_with_request=true'; \
	} >> /etc/php/7.3/fpm/php.ini


RUN apt-get update && apt-get install -y telnet php7.3-bcmath && rm -rf /var/lib/apt
