ARG VERSION
FROM gcr.io/prysmaticlabs/prysm/beacon-chain$VERSION as binary

FROM alpine

# Install dependencies
RUN apk --update add bash ca-certificates libc6-compat gcompat libstdc++ libgcc && \
    rm  -rf /tmp/* /var/cache/apk/*

COPY --from=binary /app/beacon-chain/image.binary /usr/local/bin/beacon-chain

ENTRYPOINT [ "sh", "-c", "exec beacon-chain --datadir=/data --log-file=/data/beacon-chain.log $EXTRA_OPTS" ]