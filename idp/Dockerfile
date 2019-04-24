FROM unicon/shibboleth-idp:3.4.3-20190110

MAINTAINER Unicon, Inc.

COPY shibboleth-idp/ /opt/shibboleth-idp/
COPY shib-jetty-base/ /opt/shib-jetty-base/

# On TeamCity, the LabKey Server isn't on port 8080
ARG appAddress=localhost
ARG appPort=8080
ARG contextPath=/labkey
RUN sed -e "s%localhost\:8080\/labkey%${appAddress}\:${appPort}${contextPath}%g" /opt/shibboleth-idp/metadata/lk-metadata.xml