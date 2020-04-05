# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080
LABEL io.openshift.expose-services="8080:http"
LABEL io.k8s.description="A BASIC aPACHE http sERVER CHILD IMAGE, USES onbuild" \
io.k8s.display-name="aPACHE http sERVER" \
io.openshift.expose-services="8080:http" \
io.openshift.tags="apache, httpd"

RUN sed -i "s/listen 80/listen 8080/g" /etc/httpd/conf/httpd.conf
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001


