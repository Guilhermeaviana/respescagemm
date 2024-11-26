# Usa a imagem oficial do Node.js
FROM node:18

# Define o diretório de trabalho dentro do contêiner
WORKDIR /app

# Copia os arquivos do projeto para dentro do contêiner
COPY package*.json ./

# Instala as dependências
RUN npm install

# Copia o restante do código do backend
COPY . .

# Define a porta que o app escuta
EXPOSE 3000

# Comando para iniciar a aplicação
CMD ["npm", "start"]
