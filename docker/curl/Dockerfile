FROM alpine:latest

RUN apk add --no-cache \
  nghttp2 \
  libssh2 \
  ca-certificates \
  curl

RUN addgroup -S curl_group && adduser -S curl_user -G curl_group

USER curl_user

COPY "entrypoint.sh" "/entrypoint.sh"
ENTRYPOINT ["/entrypoint.sh"]
CMD ["curl"]
