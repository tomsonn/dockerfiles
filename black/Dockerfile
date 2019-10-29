FROM python:3.7-alpine

RUN apk add --no-cache --virtual=.build-deps build-base && \
    addgroup -S black && adduser -D -S black black && \
    pip install --no-cache-dir black==19.10b0 && \
    apk del .build-deps && \
    mkdir /src

USER black

CMD ["black"]
LABEL name=black version=19.10b0 \
    maintainer="Alex Viscreanu <aexvir@kiwi.com>"
