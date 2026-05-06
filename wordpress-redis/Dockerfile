FROM wordpress:latest

RUN pecl install redis && docker-php-ext-enable redis

RUN useradd --system --uid 1000 --gid 33 wordpress-nonroot

RUN chown -R 1000:33 /var/www/html

USER 1000:33
