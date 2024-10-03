FROM ubi8/php-74
#ADD ./src /opt/app-root/src
RUN wget https://es-mx.wordpress.org/latest-es_MX.zip
RUN unzip latest-es_MX.zip
RUN mv wordpress/* .
WORKDIR /opt/app-root/src/wordpress
USER 0
RUN chgrp -R 0 /opt/app-root/src && \
    chmod -R g+rwX /opt/app-root/src