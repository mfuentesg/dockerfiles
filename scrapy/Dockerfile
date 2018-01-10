FROM python:3.6-alpine

RUN apk add --no-cache build-base libxslt-dev libxml2-dev openssl-dev libffi-dev && \
    pip install scrapy && \
    # clean up
    apk del build-base && rm -f /var/cache/apk/*
