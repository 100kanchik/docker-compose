FROM openjdk:8-jre-alpine
WORKDIR /usr/local/tomcat
RUN wget https://mirrors.nav.ro/apache/tomcat/tomcat-8/v8.5.65/bin/apache-tomcat-8.5.65.tar.gz  -O /tmp/tomcat.tar.gz && cd /tmp && tar xvfz /tmp/tomcat.tar.gz && cp -Rv /tmp/apache-tomcat-8.5.65/* /usr/local/tomcat/ && rm -rf /tmp/* /usr/local/tomcat/webapps/docs/* /usr/local/tomcat/webapps/examples/*
EXPOSE 8080
CMD  cp -r /usr/local/pack/* /usr/local/tomcat/webapps/  && /usr/local/tomcat/bin/catalina.sh run