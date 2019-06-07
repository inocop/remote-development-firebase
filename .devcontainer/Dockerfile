FROM ubuntu:18.04

MAINTAINER inocop

# Configure apt
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
&&  apt-get -y install --no-install-recommends apt-utils 2>&1

# Install git, process tools, lsb-release (common in install instructions for CLIs)
RUN apt-get -y install git \
                       curl \
                       procps \
                       lsb-release \
# install node \
&&  curl --silent --location https://deb.nodesource.com/setup_8.x | bash - \
&&  apt-get install -y nodejs \
# Clean up \
&&  apt-get autoremove -y \
&&  apt-get clean -y \
&&  rm -rf /var/lib/apt/lists/*

# install node_modules
RUN npm install -g firebase-tools \
                   eslint

# Set the default shell to bash instead of sh
ENV SHELL /bin/bash
ENV DEBIAN_FRONTEND=dialog