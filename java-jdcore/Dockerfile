FROM openjdk:alpine
MAINTAINER Marcelo Fuentes <marceloe.fuentes@gmail.com>

RUN apk add --no-cache --virtual .build-deps bash mercurial && \
    wget -O master.zip https://github.com/nviennot/jd-core-java/archive/master.zip && \
    unzip master.zip && cd `pwd`/jd-core-java-master && ./gradlew assemble && cd - && \
    mv `pwd`/jd-core-java-master/build/libs/jd-core-java-1.2.jar /usr/local/lib/ && \
    alias jdcore="java -jar /usr/local/lib/jd-core-java-1.2.jar" && \
    # Clean up
    apk del .build-deps && rm -rf `pwd`/jd-core-java-master `pwd`/master.zip

CMD ["jdcore"]
