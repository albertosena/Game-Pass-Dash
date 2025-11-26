# backend/Dockerfile
FROM node:20-alpine

# Diretório de trabalho dentro do container
WORKDIR /usr/src/app

# Copia apenas os manifests primeiro (cache de dependências)
COPY package*.json ./

# Instala dependências (incluindo dev, já que o script é "dev")
RUN npm install

# Copia o restante do código
COPY . .

# Porta que a API expõe
ENV PORT=4000
EXPOSE 4000

# Comando para iniciar o servidor
CMD ["npm", "run", "dev"]
