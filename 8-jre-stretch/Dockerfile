FROM openjdk:8-jre-stretch

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN \
    curl -sL -o ~/checkstyle.jar https://repo1.maven.org/maven2/com/puppycrawl/tools/checkstyle/8.9/checkstyle-8.9.jar

RUN \
    mkdir -p /root/.ssh \
    && chmod 700 /root/.ssh \
    && echo "" > /root/.ssh/known_hosts
