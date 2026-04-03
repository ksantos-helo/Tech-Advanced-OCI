# Preparando o ambiente

## 1 - Instalando o Node.js

O Node.js é um ambiente de execução Javascript, ou seja, um lugar fora do navegador em que podemos executar a linguagem. Dessa forma, é uma plataforma na qual podemos executar códigos que utilizam essa linguagem do lado do servidor (ou server-side).

Vamos utilizá-lo aqui para executar o projeto All Books do lado do servidor.

Para fazer a instalação, Confira o artigo: [Como instalar o Node.js no Windows, Linux e macOS.](https://www.alura.com.br/artigos/como-instalar-node-js-windows-linux-macos)

O projeto do All Books está dividido em duas partes: frontend e backend. Você deve fazer o download e executar cada uma dessas partes em seu computador.

## 2 - Baixando e executando o Backend

Abra um terminal em seu computador e execute os seguintes comandos:

```
# baixando o backend
git clone https://github.com/alura-cursos/api-alurabooks.git

# acessando a pasta do backend
cd api-alurabooks

# instalando as dependências listadas no arquivo package.json
npm install

# executando o backend e o disponibilizando através de um servidor no endereço http://localhost:8000
npm run start-auth
Copiar código
```

## 3 - Baixando e executando o Frontend

Agora você deve abrir outro terminal e executar os comandos listados abaixo:
```
# baixando o frontend do projeto
git clone https://github.com/alura-cursos/curso-react-alurabooks.git

# acessando a pasta do frontend
cd curso-react-alurabooks

# selecionando a versão correta
git checkout aula-5

# instalando as dependências
npm install

# compilando o frontend e o disponibilizando através de um servidor no endereço http://localhost:3000
npm start
Copiar código
```

Depois dessa sequência de passos, você estará com tudo pronto para embarcar na jornada pelo mundo DevOps!

Acesse o endereço http://localhost:3000/ em seu navegador para conferir o projeto All Books!
