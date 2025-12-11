FROM mcr.microsoft.com/devcontainers/universal:2-linux

# Use root to install system + language tools
USER root

# 1) System packages
RUN apt-get update && apt-get install -y xz-utils

# 2) Vue.js tooling (Vue CLI)
# universal:2-linux already includes Node + npm
RUN npm install -g @vue/cli

# 3) Flask (Python web framework)
RUN pip3 install Flask

# Go back to normal dev user
USER vscode

# Default working directory inside the container
WORKDIR /workspaces/fouad_aoude
