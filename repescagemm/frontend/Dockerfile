# Usa uma imagem com o Node.js para construir o projeto
FROM node:18 as build

# Define o diretório de trabalho
WORKDIR /app

# Copia os arquivos do projeto
COPY package*.json ./

# Instala as dependências
RUN npm install

# Copia o restante do código e executa o build
COPY . .
RUN npm run build

# Usa uma imagem leve para servir o frontend
FROM nginx:alpine

# Copia o build gerado para o Nginx
COPY --from=build /app/build /usr/share/nginx/html

# Expõe a porta do servidor
EXPOSE 80

# Comando padrão para o Nginx
CMD ["nginx", "-g", "daemon off;"]
