# Gerar imagem e executar container - app php

## 1. Gerar imagem docker: <br/>
```sudo docker build -t app-php .```
## 2. Executar o container:<br/>
```sudo docker run -d -p 8080:80 --name app-php --rm app-php```
## 3. Executar e Atualizar o projeto em tempo real:
```sudo docker run -d -p 8080:80 --name app-php --rm -v <informe-o-diretorio-raiz-do-projeto>:/var/www/html app-php```
## 4. Executar e Visualizar os arquivos de texto no projeto em tempo real:
```sudo docker run -d -p 8080:80 --name app-php --rm -v <informe-o-diretorio-raiz-do-projeto>/messages:/var/www/html/messages app-php```