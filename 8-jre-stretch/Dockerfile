FROM openjdk:8-jre-stretch

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN \
    curl -sL -o ~/checkstyle.jar https://downloads.sourceforge.net/project/checkstyle/checkstyle/8.10/checkstyle-8.10-all.jar

RUN \
    mkdir -p /root/.ssh \
    && chmod 700 /root/.ssh \
    && echo "" > /root/.ssh/known_hosts
