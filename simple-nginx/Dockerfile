FROM rhel9/nginx-120
RUN echo "<h1>hi world</h1>">/opt/app-root/src/index.html
RUN chgrp -R 0 /opt/app-root/src && \
    chmod -R g+rwX /opt/app-root/src