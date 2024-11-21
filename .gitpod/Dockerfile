# hadolint ignore=DL3006
FROM gitpod/workspace-full

ARG TASK_VERSION=3.40.0

USER root

RUN wget -q -P /tmp https://github.com/go-task/task/releases/download/v$TASK_VERSION/task_linux_amd64.deb && \
    dpkg -i /tmp/task_linux_amd64.deb && \
    rm -f /tmp/task_linux_amd64.deb

USER gitpod
