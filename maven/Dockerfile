FROM ubuntu:latest
RUN apt-get update && apt-get install maven git -y
WORKDIR /usr/local/
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
WORKDIR /usr/local/boxfuse-sample-java-war-hello/
RUN  mvn package
WORKDIR /usr/local/webapps/
RUN cp ./target/hello-1.0.war /usr/local/tomcat/webapps/ && cp -r ./target/hello-1.0 /usr/local/tomcat/webapps/hello-1.0