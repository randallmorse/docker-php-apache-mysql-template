FROM php:8.1-apache
#install mysql extensions
RUN apt-get update && \
    docker-php-ext-install mysqli pdo pdo_mysql
#install gd extensions
RUN apt-get update && apt-get install -y \
		libfreetype6-dev \
		libjpeg62-turbo-dev \
		libpng-dev \
	&& docker-php-ext-configure gd --with-freetype --with-jpeg \
	&& docker-php-ext-install -j$(nproc) gd