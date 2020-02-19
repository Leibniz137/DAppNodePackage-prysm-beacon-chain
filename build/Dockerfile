ARG SHA256
FROM gcr.io/prysmaticlabs/prysm/beacon-chain@$SHA256 as binary

FROM alpine

# Install dependencies
RUN apk --update add bash ca-certificates libc6-compat && \
    rm  -rf /tmp/* /var/cache/apk/*

COPY --from=binary /app/beacon-chain/image.binary /usr/local/bin/beacon-chain

ENTRYPOINT beacon-chain --datadir=/data --init-sync-no-verify $EXTRA_OPTS
