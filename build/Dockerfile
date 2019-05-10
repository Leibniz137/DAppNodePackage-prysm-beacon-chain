FROM openjdk:8 as build

# Install Bazel and dependencies
RUN echo "deb [arch=amd64] http://storage.googleapis.com/bazel-apt stable jdk1.8" | tee /etc/apt/sources.list.d/bazel.list  && \
    curl https://bazel.build/bazel-release.pub.gpg | apt-key add - && \
    apt-get update && \
    apt-get install -y bazel git patch bash && \
    rm -rf /var/lib/apt/lists/*

# Set up workspace
WORKDIR /usr/src/app
ENV BRANCH master
RUN git clone -b ${BRANCH} https://github.com/prysmaticlabs/prysm.git /usr/src/app && \
    bazel build //beacon-chain:beacon-chain

FROM alpine

# Install dependencies
RUN apk --update add bash ca-certificates libc6-compat bash supervisor && \
    rm  -rf /tmp/* /var/cache/apk/*

#Copy binaries from build stage
COPY --from=build /usr/src/app/bazel-bin/beacon-chain/linux_amd64_stripped/beacon-chain /usr/local/bin/beacon-chain

COPY supervisord.conf /etc/supervisord.conf
ENTRYPOINT ["supervisord","-c","/etc/supervisord.conf"]
