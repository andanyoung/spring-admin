FROM openjdk:8-jdk-alpine

MAINTAINER 1218853253@qq.com

ARG JAR_FILE
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

EXPOSE 9090

ADD ${JAR_FILE} app.jar

VOLUME /var/log/spring-admin

ENTRYPOINT /usr/bin/java -Djava.security.egd=file:/dev/./urandom -jar app.jar