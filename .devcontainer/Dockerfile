# Use Node.js LTS base image
FROM mcr.microsoft.com/vscode/devcontainers/typescript-node:0-18

# Instalar dependências do sistema
RUN apt-get update && apt-get install -y \
  curl \
  git \
  unzip \
  && rm -rf /var/lib/apt/lists/*

# Instalar Prisma CLI globalmente
RUN npm install -g prisma

# Criar diretório de trabalho
WORKDIR /workspace

# Ajustar permissões (vscode usa usuário 'node')
USER node
