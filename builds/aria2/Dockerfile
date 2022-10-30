FROM alpine:3
ARG USER=aria

RUN apk update && apk add --no-cache --update aria2
WORKDIR /.aria2

EXPOSE 50100

ENTRYPOINT [ "aria2c", "--conf-path=/.aria2/aria2.conf" ]