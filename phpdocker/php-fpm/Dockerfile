FROM phpdockerio/php:8.1-fpm
WORKDIR "/application"

RUN apt-get update; \
    apt-get -y --no-install-recommends install \
        php8.1-gd \ 
        php8.1-imagick \ 
        php8.1-mysql \
        php8.1-intl \
        php8.1-bcmath; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

 COPY ./php-ini-overrides.ini /etc/php/8.1/fpm/conf.d/
# RUN mv /etc/php/8.1/fpm/php-ini-overrides.ini /etc/php/8.1/fpm/99-overrides.ini