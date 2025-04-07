FROM mcr.microsoft.com/devcontainers/python:3.12

USER root

### Install dependencies ###
# hadolint ignore=DL3008
RUN apt-get update -y && apt-get upgrade -y && \
    apt-get install -y --no-install-recommends \
    wget && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

### Install Task (https://taskfile.dev/) ###
RUN sh -c "$(curl --location https://taskfile.dev/install.sh)" -- -d -b /usr/local/bin && \
    bash -c "task --completion bash > /etc/bash_completion.d/task"

# hadolint ignore=DL3013
RUN pip install --no-cache-dir --upgrade pip poetry

USER vscode
