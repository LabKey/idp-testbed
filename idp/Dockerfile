FROM unicon/shibboleth-idp:3.4.3-20190110

COPY shibboleth-idp/ /opt/shibboleth-idp/
COPY shib-jetty-base/ /opt/shib-jetty-base/


ARG baseServerURL=http://localhost:8080
ARG contextPath
RUN sed -i -e "s%\${baseServerURL}%${baseServerURL}%g" -e "s%\${contextPath}%${contextPath}%g" /opt/shibboleth-idp/metadata/lk-metadata.xml
