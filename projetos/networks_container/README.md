# Criar Network

1. No terminal execute o seguinte comando:<br/>
```sudo docker network create flask-network```

# Gerar imagem e executar container - flask api

## 1. Entre na pasta flask: <br/>
```cd flask```
## 2. Gerar imagem docker: <br/>
```sudo docker build -t flask-api .```
## 3. Executar o container:<br/>
```sudo docker run -d -p 5000:5000 --name flask-api --rm flask-api```
## 4. Adicione o container a rede criada:<br/>
```sudo docker network connect flask-network flask-api```
## 5. Verifique que o container flask-api está conectado ao network criado:<br/>
```sudo docker inspect flask-api```

# Gerar imagem mysqldb api

## 1. Entre na pasta flask: <br/>
   ```cd mysql```
## 2. Gerar imagem docker: <br/>
   ```sudo docker build -t mysqldb-flask-api .```
## 3. Executar o container:<br/>
#### OBS: Caso tenha o MySQL instalado na máquina, é necessário informar a porta 3307 ao gerar o container.<br/>
   ```sudo docker run -d -p 3307:3306 --name mysql-api --rm -e MYSQL_ALLOW_EMPTY_PASSWORD=True mysqldb-flask-api```
## 4. Adicione o container a rede criada:<br/>
   ```sudo docker network connect flask-network mysql-api```
## 5. Verifique se o container está conectado ao network criado:<br/>
   ```sudo docker inspect mysql-api```