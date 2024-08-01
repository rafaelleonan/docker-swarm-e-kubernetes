# Gerar imagem e executar container - api flask externa

## 1. Gerar imagem docker: <br/>
```sudo docker build -t api-flask-externa .```
## 2. Executar o container:<br/>
```sudo docker run -d -p 5000:5000 --name api-flask-externa --rm api-flask-externa```