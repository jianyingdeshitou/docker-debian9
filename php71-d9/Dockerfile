FROM debian9

MAINTAINER 坚硬的石头 <do_nb@outlook.com>

RUN apt-get update \
	&& apt-get -y install apt-transport-https lsb-release ca-certificates \
	&& wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg \
	&& sh -c 'echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list' \
	&& rm -rf /var/lib/apt/lists/*

RUN apt-get update \
    && apt-get install -y php7.1 php7.1-cli php7.1-common php7.1-fpm php7.1-cgi \
        php7.1-mysql php7.1-curl php7.1-gd php7.1-imagick php7.1-zip php7.1-gmp \
        php7.1-imap php7.1-mcrypt php7.1-memcache php7.1-pspell php7.1-recode \
        php7.1-xml php7.1-xsl php7.1-json php7.1-mbstring \
    && rm -rf /var/lib/apt/lists/*

ENV PATH "/composer/vendor/bin:$PATH"
ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_HOME /composer

RUN curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer 
RUN composer config -g repo.packagist composer https://packagist.phpcomposer.com

