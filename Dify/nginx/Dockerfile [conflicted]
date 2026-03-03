FROM nginx:latest

RUN set -eux \
    && apt-get update \
    && apt-get install -y --no-install-recommends curl \
    && curl -L https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64 -o /usr/local/bin/cloudflared \
    && chmod +x /usr/local/bin/cloudflared \
    && apt-get purge -y --auto-remove curl \
    && rm -rf /var/lib/apt/lists/*
