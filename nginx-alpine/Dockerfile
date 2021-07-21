FROM nginx:1.20.1-alpine

COPY nginx.conf /etc/nginx/nginx.conf
COPY ssl/ /etc/nginx/ssl/
COPY default_403.conf /etc/nginx/conf.d/default_403.conf
COPY proxy.conf /etc/nginx/proxy.conf

ENV TZ Asia/Shanghai

RUN echo "https://repo.huaweicloud.com/alpine/v3.13/main/" > /etc/apk/repositories \
	&& echo "https://repo.huaweicloud.com/alpine/v3.13/community/" >> /etc/apk/repositories \
	&& apk add --no-cache tzdata \
	&& cp /usr/share/zoneinfo/${TZ} /etc/localtime \
	&& echo ${TZ} > /etc/timezone \
	&& apk del tzdata

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]