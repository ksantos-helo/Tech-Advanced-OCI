# 🌐📡 Resumo — CRUD, HTTP Stateless e Autenticação

## 🧠 Conceitos principais
- CRUD: operações fundamentais em sistemas:
  - Create (criar)
  - Read (ler)
  - Update (atualizar)
  - Delete (deletar)
- Usado em:
  - Aplicações web
  - Bancos de dados
  - Infraestrutura como código (ex: Terraform)

---

## 🔐 Acesso restrito e autenticação
- Áreas como **"Minha Conta"** possuem dados sensíveis
- Necessário validar o usuário com:
  - Login (email + senha)
  - Token de acesso

---

## ⚠️ Problema encontrado (Postman)
- Requisição:
```http
  GET http://localhost:8000/pedidos
```
Resposta:
 ```
{
  "status": 401,
  "message": "Token inválido"
}
 ```
👉 Motivo: requisição sem autenticação

## 🧠 Stateless (sem estado)
Servidores HTTP não armazenam informações anteriores

Cada requisição precisa:

Informar quem é o usuário

Enviar credenciais novamente

📌 Analogia:

Como uma pulseira em evento → você mostra sempre que precisa acessar algo

🔑 Formas de autenticação
### 1️⃣ Token (Bearer)
Gerado via login (POST)

Enviado em todas as requisições
 ```
Authorization: Bearer SEU_TOKEN
 ```

### 2️⃣ Cookies
Armazenados no navegador

Usados para identificar o usuário automaticamente

## 🔄 Fluxo correto no Postman
### 1. Gerar token (login)
```
POST http://localhost:8000/public/login
```
Body:

 ```
{
  "email": "lcs@alura.com",
  "senha": "123"
}
 ```

### 2. Usar o token
Ir em Headers

Adicionar:

Key	Value
Authorization	Bearer SEU_TOKEN
### 3. Fazer requisição autenticada
 ```
GET http://localhost:8000/pedidos
 ```

✅ Resultado:

Retorno dos dados em JSON (pedidos)

### 🔒 Segurança
Nunca usar senhas fracas (ex: 123)

Implementar:

Autenticação

Autorização

Proteção de dados

### 🚀 Resumo final
HTTP é stateless

Sempre enviar autenticação

Token valida acesso

Postman exige configuração correta (Headers)
