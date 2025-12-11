FROM mcr.microsoft.com/devcontainers/universal:2-linux
# Install the xz-utils package
RUN apt-get update && apt-get install -y xz-utils curl

# Install Node.js (LTS) + npm
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs

# Install Vue CLI globally
RUN npm install -g @vue/cli

RUN pip install --no-cache-dir flask

# Set working directory
WORKDIR /workspace