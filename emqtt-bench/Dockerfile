FROM erlang:22-alpine

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
    && apk add --no-cache bash bash-doc bash-completion git make \
    && git clone https://github.com/emqx/emqtt-bench.git \
    && cd emqtt-bench/ && make

CMD ["/bin/bash"]
