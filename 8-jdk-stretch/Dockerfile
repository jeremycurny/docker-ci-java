FROM openjdk:8-jdk-stretch

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN  \
    apt-get update \
    && apt-get install -y \
        maven \
    && curl -sL https://deb.nodesource.com/setup_8.x | bash \
    && apt-get install -y nodejs \
    && apt-get clean autoclean \
    && apt-get autoremove

RUN \
    cd \
    && curl -sL -o ~/checkstyle.jar https://downloads.sourceforge.net/project/checkstyle/checkstyle/8.10/checkstyle-8.10-all.jar \
    && curl -sL -o ~/pmd-bin-6.3.0.zip https://github.com/pmd/pmd/releases/download/pmd_releases%2F6.3.0/pmd-bin-6.3.0.zip \
    && unzip pmd-bin-6.3.0.zip \
    && rm pmd-bin-6.3.0.zip \
    && mv pmd-bin-6.3.0 pmd-bin

RUN \
    npm install -g serverless serverless-domain-manager

RUN \
    mkdir -p /root/.ssh \
    && chmod 700 /root/.ssh \
    && echo "" > /root/.ssh/known_hosts
