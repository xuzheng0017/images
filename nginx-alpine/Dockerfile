FROM nginx:1.20.1-alpine

COPY nginx.conf /etc/nginx/nginx.conf
COPY ssl/ /etc/nginx/ssl/
COPY conf.d/ /etc/nginx/conf.d/
COPY proxy.conf /etc/nginx/proxy.conf
COPY deny.conf /etc/nginx/deny.conf

ENV TZ Asia/Shanghai

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
	&& apk add --no-cache tzdata \
	&& cp /usr/share/zoneinfo/${TZ} /etc/localtime \
	&& echo ${TZ} > /etc/timezone \
	&& apk del tzdata

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]