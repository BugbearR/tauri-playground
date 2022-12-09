FROM mcr.microsoft.com/devcontainers/typescript-node:16-bullseye

ENV PATH="/root/.cargo/bin:$PATH"

RUN apt-get update -y \
    && DEBIAN_FRONTEND=noninteractive apt-get upgrade -y \
    && apt-get install -y --no-install-recommends \
        ca-certificates \
        curl \
        gnupg2 \
    && apt-get clean \
    && rm -rf /var/cache/apt/* /var/lib/apt/lists/

# RUN curl https://sh.rustup.rs -sSf | sh -s --

USER node

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y \
    && npm install -g pnpm
