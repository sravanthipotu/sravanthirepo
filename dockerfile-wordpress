FROM wordpress:php8.2-apache
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
COPY wp-config.php /var/www/html/wp-config.php
HEALTHCHECK --interval=30s --timeout=5s --retries=3 CMD curl -f http://localhost/ || exit 1
