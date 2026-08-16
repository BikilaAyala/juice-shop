FROM alpine

RUN apk add --no-cache curl \
    && addgroup -S nonroot \
    && adduser -S nonroot -G nonroot

COPY smoke-test.sh smoke-test.sh

USER nonroot

CMD ["sh", "smoke-test.sh", "http://app:3000"]
