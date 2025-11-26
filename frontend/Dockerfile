# frontend/Dockerfile
FROM node:20-alpine

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install

# Copia o restante do frontend
COPY . .

# Porta do Vite dev server
EXPOSE 5173

# Sobe o Vite acessível pela rede
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0", "--port", "5173"]
