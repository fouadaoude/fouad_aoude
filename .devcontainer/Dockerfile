FROM mcr.microsoft.com/devcontainers/universal:2-linux

# --- use root so installs don't fail ---
USER root

# 1) System packages + Node.js + npm + Python pip
RUN apt-get update && apt-get install -y \
    xz-utils \
    curl \
    nodejs \
    npm \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

# 2) Vue CLI (Vue.js tooling)
RUN npm install -g @vue/cli

# 3) Flask (Python web framework)
RUN pip3 install Flask

# --- go back to normal dev user ---
USER vscode

# Default working directory in the container
WORKDIR /workspaces/fouad_aoude
