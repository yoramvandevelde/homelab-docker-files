FROM alpine:3.21

RUN apk add --no-cache \
    curl \
    bash \
    gnupg \
    kubectl \
    helm \
    && curl -Lo /usr/local/bin/talosctl \
       https://github.com/siderolabs/talos/releases/latest/download/talosctl-linux-amd64 \
    && chmod +x /usr/local/bin/talosctl

ENTRYPOINT ["bash"]
