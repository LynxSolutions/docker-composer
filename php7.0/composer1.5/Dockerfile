# Pull base image.
FROM lynxsolutions/composer
MAINTAINER Nimrod Nagy <nimrod.nagy@lynxsolutions.eu>

# Install rsync for deployment
RUN apk --no-cache add openssh-client rsync openssl zlib-dev icu-dev libxml2-dev g++ autoconf openssl-dev make pcre-dev libpng-dev libmcrypt-dev

RUN docker-php-ext-configure intl

RUN docker-php-ext-configure intl
RUN docker-php-ext-configure soap --enable-soap

#install mysql pdo
RUN docker-php-ext-install pdo pdo_mysql bcmath soap pcntl gd mcrypt exif sockets

#install mongodb php extension
RUN pecl install mongodb-1.2.9 \
  && docker-php-ext-enable mongodb

# Set correct entrypoint
CMD ["/bin/bash"]
ENTRYPOINT []
