Newman é uma ferramenta de linha de comando para executar Postman Collections. 
Use Newman para executar e testar coleções a partir da linha de comando em vez de no aplicativo Postman.


GitHub Action:
GitHub Actions é uma ferramenta de CI/CD (Continuous Integration/Continuous Deployment) integrada ao GitHub.


O que o GitHub Actions faz?
Ele permite automatizar fluxos de trabalho, como:
🔹 CI (Continuous Integration) → Testar e validar código automaticamente sempre que há um commit/pull request.
🔹 CD (Continuous Deployment/Delivery) → Implantar aplicações automaticamente em servidores, serviços na nuvem (AWS, Azure, etc.), ou em containers (Docker, Kubernetes).
🔹 Automação Geral → Criar rotinas para publicar pacotes, enviar notificações, formatar código, entre outros.



comandos:

newman run <nome arquivo exportado na pasta local>
newman run arquivo-teste-collection.json


newman run <URL>
https://api.postman.com/collections/url aqui


CRIANDO UM PROJETO NO VS CODE:

1- Crie uma pasta do projeto
2- Inicialize um projeto Node.js nesta pasta pelo terminal:  npm init -y   (um arquivo package.json é criado
3- Instale o Newman no projeto:  npm install -g newman
4- No VS Code, crie a pasta .github/workflows/
5- Crie o arquivo do pipeline: YML
6- Subir o Projeto para o GitHub. Criar um repositório no GitHub (projeto-test-newman)
7- No terminal do VS Code, rode os seguintes comandos:




Conteudo arquivo YML

name: API Tests with Newman

on:
  push:
    branches: [ main ]
  pull_request:

jobs:
  test-api:
    runs-on: ubuntu-latest  

    steps:
      - name: Clonar repositório
        uses: actions/checkout@v3  

      - name: Instalar Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '20'

      - name: Instalar Newman
        run: npm install -g newman  

      - name: Rodar Testes da API
        run: newman run collections/postman-collection-test.json -r cli,json  
