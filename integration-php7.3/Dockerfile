FROM nextcloudci/php7.3:php7.3-5

RUN composer global require hirak/prestissimo

RUN mkdir /tmp/server && \
    cd /tmp/server && git clone --recursive https://github.com/nextcloud/server.git && \
    cd /tmp/server/server/build/integration && composer install && \
    cd /tmp/server/server/tests/acceptance && composer install && \
    rm -rf /tmp/server
