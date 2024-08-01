# Gerar imagem e executar container - app nodejs

## 1. Gerar imagem docker: <br/>
```sudo docker build -t app-nodejs .```
## 2. Executar o container:<br/>
```sudo docker run -d -p 3000:3000 --name app-nodejs --rm app-nodejs```