FROM alpine:3.21.3
RUN apk add --no-cache curl && \
    curl -sSfL https://github.com/anchore/syft/releases/download/v1.44.0/syft_1.44.0_linux_amd64.tar.gz | tar xz -C /usr/local/bin syft && \
    curl -sSfL https://github.com/sigstore/cosign/releases/download/v3.0.6/cosign-linux-amd64 -o /usr/local/bin/cosign && \
    chmod +x /usr/local/bin/cosign && \
    apk del curl
