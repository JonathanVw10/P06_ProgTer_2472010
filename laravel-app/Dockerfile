FROM php:8.4-cli

RUN apt-get update && apt-get install -y \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    unzip \
    curl \
    sqlite3 \
    libsqlite3-dev

RUN docker-php-ext-install pdo pdo_sqlite mbstring

WORKDIR /app

COPY . /app

EXPOSE 8000

CMD ["php", "artisan", "serve", "--host=0.0.0.0", "--port=8000"]
