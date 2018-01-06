FROM php71-d9

MAINTAINER 坚硬的石头 <do_nb@outlook.com>

RUN apt-get update \
    && apt-get install -y php7.1-dev php7.1-xdebug \
    && rm -rf /var/lib/apt/lists/*

VOLUME /app
WORKDIR /app
