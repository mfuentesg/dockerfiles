FROM python:3.6-alpine as compiler

RUN apk add --no-cache build-base libxslt-dev libxml2-dev && \
    pip install lxml && \
    # clean up
    apk del build-base && rm -f /var/cache/apk/*
