FROM emscripten/emsdk:3.1.8

# Config

ARG USERNAME=vscode
ARG USER_UID=2000
ARG USER_GID=$USER_UID

# DevContainer

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd -s /bin/bash --uid $USER_UID --gid $USER_GID -m $USERNAME \
    && apt-get install -y sudo \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME\
    && chmod 0440 /etc/sudoers.d/$USERNAME
