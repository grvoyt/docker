FROM php:7.4-fpm

# Install Composer (including ZIP for Composer)
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN apt-get update && apt-get install -y \
libfreetype6-dev \
libjpeg62-turbo-dev \
libxslt-dev \
libicu-dev \
libmcrypt-dev \
libpng-dev \
libxml2-dev \
git \
libzip-dev \
libonig-dev

RUN docker-php-ext-install -j$(nproc) exif iconv mbstring mysqli pdo_mysql json zip

RUN docker-php-ext-configure intl
RUN docker-php-ext-install intl
RUN docker-php-ext-install xsl
