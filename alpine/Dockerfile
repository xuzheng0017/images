FROM alpine:3.12

COPY glibc-2.34-r0.apk /opt/glibc-2.34-r0.apk
COPY glibc-bin-2.34-r0.apk /opt/glibc-bin-2.34-r0.apk

RUN echo "https://mirrors.aliyun.com/alpine/v3.12/main/" > /etc/apk/repositories \
    && apk add --no-cache ca-certificates tzdata libstdc++ \
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo "Asia/Shanghai" > /etc/timezone \
    && apk add --allow-untrusted /opt/glibc-2.34-r0.apk /opt/glibc-bin-2.34-r0.apk \
    && /usr/glibc-compat/sbin/ldconfig /lib /usr/glibc-compat/lib
