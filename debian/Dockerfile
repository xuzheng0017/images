FROM debian:buster

ENV TZ=Asia/Shanghai \
    DEBIAN_FRONTEND=noninteractive

ADD sources.list /etc/apt/sources.list

RUN apt install apt-transport-https ca-certificates \
    && ln -fs /usr/share/zoneinfo/${TZ} /etc/localtime \
    && echo ${TZ} > /etc/timezone \
    && dpkg-reconfigure --frontend noninteractive tzdata \
    && rm -rf /var/lib/apt/lists/*
