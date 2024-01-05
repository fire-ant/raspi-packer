# syntax=docker/dockerfile:1

# ARGS
ARG dagv=0.9.5

FROM mcr.microsoft.com/devcontainers/base:bullseye
RUN apt-get update && apt-get install --no-install-recommends -y \
  curl=7.74.0-1.3+deb11u7 \
  jq=1.6-2.1 \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*
# dagger
RUN curl -L https://dl.dagger.io/dagger/install.sh | BIN_DIR=/usr/bin VERSION="${dagv}" sh