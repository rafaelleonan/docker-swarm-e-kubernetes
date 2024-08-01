# Gerar imagem e executar container - api flask host
`
## 1. Gerar imagem docker: <br/>
```sudo docker build -t api-flask-host .```
## 2. Executar o container:<br/>
```sudo docker run -d -p 5000:5000 --name api-flask-host --rm api-flask-host```