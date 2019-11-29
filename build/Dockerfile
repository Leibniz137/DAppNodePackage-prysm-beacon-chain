FROM gcr.io/prysmaticlabs/prysm/beacon-chain@sha256:7efb30a12bc1bd0e3bc87ee01f051dba790d087647996805f15e0f878829de0b as binary

FROM alpine

# Install dependencies
RUN apk --update add bash ca-certificates libc6-compat && \
    rm  -rf /tmp/* /var/cache/apk/*

COPY --from=binary /app/beacon-chain/image.binary /usr/local/bin/beacon-chain

ENTRYPOINT beacon-chain --datadir=/data --init-sync-no-verify $EXTRA_OPTS