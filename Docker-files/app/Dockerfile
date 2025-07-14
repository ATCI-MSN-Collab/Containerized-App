FROM maven:3.9.9-eclipse-temurin-21-jammy as BUILD_ARTIFACT

LABEL "App"="Prod"
LABEL "Service"="FED"

RUN git clone https://github.com/hkhcoder/vprofile-project.git
RUN cd vprofile-project && git checkout containers && mvn install

FROM tomcat:10-jdk21
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_ARTIFACT vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war