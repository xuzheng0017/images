FROM erlang:24

RUN git clone https://github.com/emqx/emqtt-bench.git \
    && cd emqtt-bench/ && make

CMD ["/bin/bash"]
