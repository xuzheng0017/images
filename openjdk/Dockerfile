FROM openjdk:8-alpine

ENV TZ Asia/Shanghai

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
	&& apk --no-cache add fontconfig ttf-dejavu tzdata \
	&& cp /usr/share/zoneinfo/${TZ} /etc/localtime \
	&& echo ${TZ} > /etc/timezone

ADD simsun.ttc /usr/share/fonts/ttf-dejavu/simsun.ttc
ADD STSONG.TTF /usr/share/fonts/ttf-dejavu/STSONG.TTF