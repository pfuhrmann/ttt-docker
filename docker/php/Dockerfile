FROM php:7.1-fpm

# Composer install.
RUN if [ ! -f /usr/bin/composer ]; then curl -sS https://getcomposer.org/installer | php && mv composer.phar /usr/bin/composer; fi

# Install server dependencies.
RUN apt-get update
RUN apt-get install -y git zip unzip curl nano net-tools
RUN pecl install xdebug-2.5.1
RUN docker-php-ext-enable xdebug
