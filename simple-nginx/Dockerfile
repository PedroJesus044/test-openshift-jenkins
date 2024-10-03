FROM rhel9/nginx-120
ADD ./src /opt/app-root/src
USER 0
RUN chgrp -R 0 /opt/app-root/src && \
    chmod -R g+rwX /opt/app-root/src