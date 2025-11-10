FROM mcr.microsoft.com/devcontainers/python:3.12

USER root

### Install dependencies ###
# hadolint ignore=DL3008
RUN apt-get update -y && apt-get upgrade -y && \
    apt-get install -y --no-install-recommends \
    wget && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# hadolint ignore=DL3013
RUN pip install --no-cache-dir --upgrade pip poetry go-task-bin

USER vscode

RUN echo 'alias ll="ls -lisa"' >> ~/.bashrc
