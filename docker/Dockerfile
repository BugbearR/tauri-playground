FROM mcr.microsoft.com/devcontainers/typescript-node:16-bullseye

ENV PATH="/root/.cargo/bin:$PATH"

RUN apt-get update -y \
    && DEBIAN_FRONTEND=noninteractive apt-get upgrade -y \
    && apt-get install -y --no-install-recommends \
        ca-certificates \
        curl \
        gnupg2 \
        build-essential \
        libdbus-1-dev \
        libssl-dev \
        libgtk-3-dev \
        libwebkit2gtk-4.0-dev \
    && apt-get clean \
    && rm -rf /var/cache/apt/* /var/lib/apt/lists/

# RUN curl https://sh.rustup.rs -sSf | sh -s --

#RUN adduser --disabled-password --gecos '' user \
#  && echo 'user ALL=(root) NOPASSWD:ALL' > /etc/sudoers.d/user
#USER user
#WORKDIR /home/user/code

USER node
#WORKDIR /home/user/code

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y \
    && npm install -g pnpm

SHELL ["/bin/bash", "-o", "pipefail", "-c"]
