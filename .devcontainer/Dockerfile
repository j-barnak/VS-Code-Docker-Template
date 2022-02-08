# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.209.6/containers/ubuntu/.devcontainer/base.Dockerfile
# [Choice] Ubuntu version (use hirsuite or bionic on local arm64/Apple Silicon): hirsute, focal, bionic
ARG VARIANT="hirsute"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# Setting Time Zone
# Necessary for CMake
ENV TZ=America/New_York
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Setting Up the System
RUN apt-get update  

# Additional Packages
RUN apt-get install -qy build-essential
RUN apt-get install -qy valgrind
RUN apt-get install -qy cmake
RUN apt-get install -qy git
RUN apt-get install -qy gdb

# Clean Up System
RUN apt-get -qy autoremove
