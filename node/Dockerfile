FROM node:12-alpine3.12

ENV TZ="Asia/Shanghai"

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
    && npm config set registry https://registry.npm.taobao.org/ \
    && npm config set disturl https://npm.taobao.org/mirrors/node/ \
    && npm config set sass_binary_site https://npm.taobao.org/mirrors/node-sass/ \
    && npm config set phantomjs_cdnurl https://npm.taobao.org/mirrors/phantomjs/ \
    && npm config set chromedriver_cdnurl https://npm.taobao.org/mirrors/chromedriver/ \
    && npm config set operadriver_cdnurl https://npm.taobao.org/mirrors/operadriver/ \
    && npm config set electron_mirror https://npm.taobao.org/mirrors/electron/ \
    && npm config set python_mirror https://npm.taobao.org/mirrors/python/ \
    && apk add --no-cache tzdata \
    && cp /usr/share/zoneinfo/${TZ} /etc/localtime \
    && echo ${TZ} > /etc/timezone \
    && apk del tzdata