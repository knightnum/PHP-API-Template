# Use the official PHP 8.2 FPM Alpine image for a small footprint
FROM php:8.2-fpm-alpine

# Install system dependencies and PHP extensions for MySQL and Graphics
RUN apk add --no-cache \
    libpng-dev libjpeg-turbo-dev freetype-dev libzip-dev icu-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) pdo_mysql mysqli gd zip intl

# Set working directory inside the container
WORKDIR /var/www/html
