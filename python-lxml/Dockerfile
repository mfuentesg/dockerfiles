FROM python:3.6-alpine as compiler

RUN apk add --no-cache build-base libxslt-dev libxml2-dev && \
    pip install lxml


FROM python:3.6-alpine
COPY --from=compiler /usr/local/lib/python3.6/site-packages/ /usr/local/lib/python3.6/site-packages/
