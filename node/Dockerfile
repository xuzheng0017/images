FROM node:12-alpine3.12

ENV TZ="Asia/Shanghai"

RUN echo "https://repo.huaweicloud.com/alpine/v3.12/main/" > /etc/apk/repositories \
    && echo "https://repo.huaweicloud.com/alpine/v3.12/community/" >> /etc/apk/repositories \
    && npm config set registry https://repo.huaweicloud.com/repository/npm/ \
    && npm config set disturl https://repo.huaweicloud.com/nodejs \
    && npm config set sass_binary_site https://repo.huaweicloud.com/node-sass \
    && npm config set phantomjs_cdnurl https://repo.huaweicloud.com/phantomjs \
    && npm config set chromedriver_cdnurl https://repo.huaweicloud.com/chromedriver \
    && npm config set operadriver_cdnurl https://repo.huaweicloud.com/operadriver \
    && npm config set electron_mirror https://repo.huaweicloud.com/electron/ \
    && npm config set python_mirror https://repo.huaweicloud.com/python \
    && apk add --no-cache tzdata \
    && cp /usr/share/zoneinfo/${TZ} /etc/localtime \
    && echo ${TZ} > /etc/timezone \
    && apk del tzdata