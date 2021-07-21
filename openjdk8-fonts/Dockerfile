FROM openjdk:8-alpine

RUN sed -i "s@http://dl-cdn.alpinelinux.org/@https://repo.huaweicloud.com/@g" /etc/apk/repositories && \
	apk --no-cache add fontconfig ttf-dejavu

ADD simsun.ttc /usr/share/fonts/ttf-dejavu/
ADD STSONG.TTF /usr/share/fonts/ttf-dejavu/

