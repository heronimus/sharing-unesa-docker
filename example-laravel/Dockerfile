FROM php:7.4
RUN apt-get update -y && apt-get install -y openssl zip unzip git libonig5 libonig-dev libzip-dev

## Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN docker-php-ext-install pdo mbstring

## Copy Laravel Apps
WORKDIR /app
COPY ./laravel-app /app
RUN composer install

## Run PHP Serve
CMD php artisan serve --host=0.0.0.0 --port=8080
EXPOSE 8080
