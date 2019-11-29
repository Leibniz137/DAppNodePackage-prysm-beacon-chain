FROM gcr.io/prysmaticlabs/prysm/beacon-chain@sha256:113a07ab26a0e269cd0aee872f24464f163db353d658e32cc990e15fe205c856 as binary

FROM alpine

# Install dependencies
RUN apk --update add bash ca-certificates libc6-compat && \
    rm  -rf /tmp/* /var/cache/apk/*

COPY --from=binary /app/beacon-chain/image.binary /usr/local/bin/beacon-chain

ENTRYPOINT beacon-chain --datadir=/data --init-sync-no-verify $EXTRA_OPTS