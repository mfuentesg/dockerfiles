FROM alpine

ENV LIBSASS_VERSION=3.4.7
ENV SASSC_VERSION=3.4.7

RUN apk add --no-cache g++ make libstdc++ && \
    wget -O libsass.zip https://github.com/sass/libsass/releases/download/${LIBSASS_VERSION}/libsass-${LIBSASS_VERSION}-src.zip && \
    wget -O sassc.zip https://github.com/sass/sassc/archive/${SASSC_VERSION}.zip && \
    unzip /libsass.zip && unzip /sassc.zip && SASS_LIBSASS_PATH=/libsass-${LIBSASS_VERSION} make -C /sassc-${SASSC_VERSION} install && \
    apk del g++ make && rm -rf /libsass* /sassc* && rm -rf /var/cache/apk/*

CMD ["sassc"]
