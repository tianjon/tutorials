FROM alpine

ENV MICRO_REGISTRY_ADDRESS 192.168.13.2:2379
ENV MICRO_BOOK_CONFIG_GRPC_ADDR 192.168.13.2:9600

RUN apk update && apk add tzdata && cp -r -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

ADD html /html
ADD orders-web /orders-web

WORKDIR /
ENTRYPOINT [ "/orders-web" ]
