FROM php:7.3.12-apache

ARG developer_uid
RUN useradd -m developer -s /bin/bash -u ${developer_uid}

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN apt -y update --fix-missing

RUN apt -y install vim mc wget git curl zip
RUN apt -y install libmcrypt4 libmcrypt-dev

RUN docker-php-ext-install pdo_mysql 
RUN docker-php-ext-install mysqli


# TO DO/CHECK
# RUN docker-php-ext-install json
# RUN docker-php-ext-install mcrypt
# RUN docker-php-ext-install pdo_sqlite
# RUN docker-php-ext-install curl
# RUN docker-php-ext-install tokenizer
# RUN docker-php-ext-install mbstring

# Install xdebug
# RUN pecl install xdebug-2.5.0
# RUN docker-php-ext-enable xdebug

# # Other PHP7 Extensions

#RUN apt -y install libsqlite3-dev libsqlite3-0 default-mysql-client

# RUN apt-get -y install zlib1g-dev
# RUN docker-php-ext-install zip

# RUN apt-get -y install libicu-dev
# RUN docker-php-ext-install -j$(nproc) intl


# RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev
# RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ 
# RUN docker-php-ext-install -j$(nproc) gd

# # Enable apache modules
# RUN a2enmod rewrite headers
