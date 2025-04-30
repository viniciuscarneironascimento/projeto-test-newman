# 🧪 Projeto: projeto-test-newman

[Repositório do projeto](https://github.com/viniciuscarneironascimento/projeto-test-newman)

---

## 📝 Descrição

Este repositório faz parte do portfólio do projeto em **Node.js** para execução de coleções do **Postman** utilizando o **Newman**. O projeto também conta com **geração automática de relatórios HTML** e **integração contínua (CI/CD)** via **GitHub Actions**.

---

## 🚀 Resultados Alcançados

- **Instalação e configuração** da arquitetura do projeto **Node.js** e do **Newman**.
- **Criação de collections de testes** no **Postman**, que foram exportadas para o projeto como arquivos **JSON** e utilizadas para a execução dos testes de API.
- **Estudo e aplicação prática** da ferramenta de linha de comando **Newman** para executar as collections.
- Utilização do **ChatGPT** para gerar comandos personalizados para a execução dos testes, facilitando a integração com o arquivo de **workflow** e a automação no processo de **CI/CD** via **GitHub Actions**.
- **Aprimoramento do arquivo de workflow** para incluir a geração de relatórios de testes, proporcionando melhor visibilidade e acompanhamento.
- **Integração do workflow com o Cypress Cloud**, permitindo o gerenciamento e monitoramento dos testes automatizados diretamente na nuvem.

---



# 📚 Informações Adicionais

## ✅ O que é o Newman?

**Newman** é uma ferramenta de linha de comando para executar **Postman Collections**. Use o Newman para executar e testar coleções diretamente na linha de comando, em vez de no aplicativo Postman.

---

## ✅ O que é o GitHub Actions?

**GitHub Actions** é uma ferramenta de **CI/CD (Integração Contínua / Entrega Contínua)** integrada ao GitHub.

### O que o GitHub Actions faz?

Ele permite automatizar fluxos de trabalho, como:

- 🔹 **CI (Continuous Integration)** → Testar e validar código automaticamente sempre que há um commit ou pull request.
- 🔹 **CD (Continuous Deployment/Delivery)** → Implantar aplicações automaticamente em servidores, serviços na nuvem (AWS, Azure, etc.), ou em containers (Docker, Kubernetes).
- 🔹 **Automação Geral** → Criar rotinas para publicar pacotes, enviar notificações, formatar código, entre outros.

---

## 💻 Comandos no Terminal

Para executar os testes com Newman, use o seguinte comando no terminal:

```bash
newman run collections/postman-collection-test.json -r cli,json


CRIANDO UM PROJETO NO VS CODE:

1- Crie uma pasta do projeto
2- Inicialize um projeto Node.js nesta pasta pelo terminal:  npm init -y   (um arquivo package.json é criado
3- Instale o Newman no projeto:  npm install -g newman
4- No VS Code, crie a pasta .github/workflows/
5- Crie o arquivo do pipeline: YML
6- Subir o Projeto para o GitHub. Criar um repositório no GitHub (projeto-test-newman)
7- No terminal do VS Code, rode os seguintes comandos:
