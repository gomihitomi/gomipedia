FROM node:20.15.1-slim

# https://code.visualstudio.com/remote/advancedcontainers/add-nonroot-user
ARG USERNAME=node

# Create the user
RUN apt-get update \
    && apt-get install -y sudo git lsof curl procps \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# ********************************************************
# * Anything else you want to do like clean up goes here *
# ********************************************************

# [Optional] Set the default user. Omit if you want to keep the default as root.
USER $USERNAME

WORKDIR /workspace
