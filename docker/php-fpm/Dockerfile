# Используем официальный образ PHP-FPM
FROM php:7.4-fpm

# Устанавливаем инструмент для работы с конфигурацией
RUN apt-get update && apt-get install -y \
    nano \
    && rm -rf /var/lib/apt/lists/*

# Копируем пользовательский php.ini в директорию конфигурации PHP
COPY ./docker/php-fpm/php.ini /usr/local/etc/php/conf.d/php.ini

# Устанавливаем рабочую директорию
WORKDIR /var/www/html