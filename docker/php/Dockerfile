FROM php:7.0.20-fpm

MAINTAINER Alessandro Galli <a.galli85@gmail.com>

RUN apt-get update \
    && apt-get install -y software-properties-common apt-transport-https \
    && apt-key adv --keyserver keyserver.ubuntu.com --recv 68576280 \
    && apt-add-repository 'deb https://deb.nodesource.com/node_6.x jessie main' \
    && apt-get update \
    && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y \
libbz2-dev \
libcurl4-openssl-dev \
libedit-dev \
libfontconfig \
libgmp-dev \
libicu-dev \
libmagickwand-dev \
libmagickcore-dev \
libmcrypt-dev \
libpng-dev \
libsqlite3-dev \
libssl-dev \
libtidy-dev \
libxml2-dev \
libxslt-dev \
libzip-dev \
curl \
zsh \
nano \
netcat \
sudo \
inotify-tools \
git \
bzip2 \
nodejs \
ssh \
openssl \
pdftk \
compass-yui-plugin \
imagemagick \
mysql-client \
    && apt-get clean \
    && docker-php-ext-install -j5 \
bcmath \
bz2 \
calendar \
ctype \
curl \
dom \
exif \
fileinfo \
ftp \
gd \
gettext \
gmp \
hash \
iconv \
intl \
json \
mbstring \
mcrypt \
mysqli \
opcache \
pcntl \
pdo_mysql \
pdo_sqlite \
posix \
readline \
session \
shmop \
simplexml \
soap \
sockets \
sysvmsg \
sysvsem \
sysvshm \
tidy \
tokenizer \
wddx \
xml \
xmlrpc \
xsl \
zip \
    && CFLAGS="-I/usr/src/php" docker-php-ext-install -j5 xmlreader \
    && pecl install \
mongodb \
    && docker-php-ext-enable \
mongodb \
    && npm install -g \
bower \
less

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

EXPOSE 9000
