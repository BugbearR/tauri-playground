FROM mcr.microsoft.com/devcontainers/typescript-node:16-bullseye

RUN apt-get update -y \
    && DEBIAN_FRONTEND=noninteractive apt-get upgrade -y \
    && apt-get clean \
    && rm -rf /var/cache/apt/* /var/lib/apt/lists/

#    && apt-get install -y git \
