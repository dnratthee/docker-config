FROM php:8.3-apache

# Set the document root
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf

# Install pdo and pdo_mysql
RUN docker-php-ext-install pdo pdo_mysql

#Enable mod_rewrite
RUN a2enmod rewrite  
