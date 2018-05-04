FROM golang:alpine as builder
LABEL mantainer="Marcelo Fuentes <marceloe.fuentes@gmail.com>"
RUN \
  echo "@edge http://dl-cdn.alpinelinux.org/alpine/edge/community" \
       >> /etc/apk/repositories && \
  apk update && apk add git build-base

# new layer makes previous cacheable
RUN go get -u github.com/pressly/goose/cmd/goose
# copy results into new image
FROM alpine
WORKDIR /data
LABEL mantainer="Marcelo Fuentes <marceloe.fuentes@gmail.com>"
COPY --from=builder /go/bin/goose /usr/local/bin/goose
COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
CMD ["goose"]