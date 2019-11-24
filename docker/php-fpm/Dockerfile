FROM php:7.2-fpm-alpine3.9

# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
# Install MySQL driver
RUN docker-php-ext-install pdo pdo_mysql
# Install PHP extensions
RUN apk add zlib-dev && docker-php-ext-install zip

RUN chmod +w -R /var/www/

EXPOSE 9000