FROM ubuntu:18.04

RUN apt-get update -y && \
apt-get install default-jre -y

ARG jarName
ARG profile
ARG serverPort
ARG dsUser
ARG dsPassword

COPY . app/
WORKDIR app

ENV JAR_NAME $jarName
ENV PROFILE $profile
ENV DATASOURCE_USER $dsUser
ENV DATASOURCE_PASSWORD $dsPassword

ENTRYPOINT java -jar $JAR_NAME \
--spring.profiles.active=$PROFILE \
--spring.datasource.username=$DATASOURCE_USER \
--spring.datasource.password=$DATASOURCE_PASSWORD

EXPOSE $serverPort