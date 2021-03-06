
# Tópicos

* [Descrição do Projeto](#descrição-do-projeto)
* [Tecnologias utilizadas](#tecnologias-utilizadas)
* [Demonstração da Aplicação](#passo-a-passo-da-aplicação)

# Descrição do Projeto
 Criação de imagem Docker baseado no projeto de conversão de temperatura da Iniciativa DevOps
 
# Tecnologias utilizadas
**nodejs**

**docker**

# Passo-a-passo da aplicação

## Passo 1
Realizar o Fork da aplicação para o seu repositório: **https://github.com/KubeDev/conversao-temperatura**

## Passo 2
Criação da imagem docker
### 2.1. Dockerfile
O Dockerfile é um documento que contém as informações necessárias para a criação da imagem, sempre utilizado a partir de uma imagem base, nesse caso, o node. Nesse caso, foram consideradas imagem oficial, idepotência.
### 2.2. Imagem
Para criar a primeira versão da imagem, utilizou-se o comando:

```docker build -t walace14/conversao-temperatura:v1 .```
### 2.3. Aplicação do container
Para executar o container utilizou-se o comando:

```docker container run -d -p 8080:8080 walace14/conversao-temperatura:v1>```

Para testar a aplicação na web, basta colocar no servidor web:

*localhost:8080*

## Passo 3
### 3.1 Repositório docker: 

Para entrar no console do Docker Hub, o seguinte comando aplicado:

```docker login```

Entrando no docker, faz-se o push da imagem:

```docker push docker push walace14/conversao-temperatura:v1``` 
### 3.2 Segunda imagem 
Para criar a segunda versão, modificou-se o index.txt e faz-se o seguinte comando:

```docker build -t walace14/conversao-temperatura:v2 .```
Novamente,fazer o push da segunda versão.
### 3.3. Aplicação do segundo container

```docker container run -d -p 8081:8080 walace14/conversao-temperatura:v2```

Para verificar a mudança, basta ir no servidor web e aplicar:

*localhost:8081*



