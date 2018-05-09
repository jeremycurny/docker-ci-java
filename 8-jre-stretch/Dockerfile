FROM openjdk:8-jre-stretch

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN \
    curl -sL -o checkstyle-8.10-all.jar https://downloads.sourceforge.net/project/checkstyle/checkstyle/8.10/checkstyle-8.10-all.jar \
    && curl -sL -o pmd-bin-6.3.0.zip https://github.com/pmd/pmd/releases/download/pmd_releases%2F6.3.0/pmd-bin-6.3.0.zip \
    && unzip pmd-bin-6.3.0.zip

RUN \
    alias checkstyle="java -jar $HOME/checkstyle-8.10-all.jar" \
    && alias pmd="$HOME/pmd-bin-6.3.0/bin/run.sh pmd"

RUN \
    mkdir -p /root/.ssh \
    && chmod 700 /root/.ssh \
    && echo "" > /root/.ssh/known_hosts
