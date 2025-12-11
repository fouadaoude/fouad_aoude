FROM mcr.microsoft.com/devcontainers/universal:2-linux

# Install the xz-utils package and curl
RUN apt-get update && \
    apt-get install -y xz-utils curl && \
    rm -rf /var/lib/apt/lists/*

# Install Node.js (LTS) + npm
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - && \
    apt-get update && \
    apt-get install -y nodejs && \
    rm -rf /var/lib/apt/lists/*

# Install Vue CLI globally
RUN npm install -g @vue/cli

# Install Flask (Python)
RUN pip install --no-cache-dir flask

# Set working directory
WORKDIR /workspace
