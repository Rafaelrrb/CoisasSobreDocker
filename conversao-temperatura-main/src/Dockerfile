FROM node:14.17.5
WORKDIR /app 
# cria um diretorio

COPY package*.json ./
# copia os arquivos 

RUN npm install
# instala o npm

COPY . .
# copia todos os arquivos restantes

EXPOSE 8080
#define uma porta

CMD ["node","server.js"]
# ordem de execução 

# crinado a imagem 
# sudo docker image buikd -t conversao-temperatura .

# rodando
# sudo docker container rum -d -p 8080:8080 conversao-temperatura

# entre usar COPY e ADD use o COPY

# uso de TEG usando argumento na contrução da imagem 
# ARG TAG=latest
# FROM ubuntu:$TAG
# RUN apt-get update && apt-get isntall curl --yes

# uso no terminal 
# sudo docker build -t rrborba/ubuntu-arg:v1 --build-arg TAG="18.04" .
