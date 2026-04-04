# IMPORTANTE

precisamos dominar são quatro métodos básicos, pilares de uma aplicação web. Inclusive, eles são bem conhecidos e formam um acrônimo que você já deve ter ouvido falar. São eles:

### ⚠️ 'Post' - Criar (Create);

### ⚠️ 'Get' - Ler (Read);

### ⚠️ 'Put' - Atualizar (Update);

### ⚠️ 'Delete' - Apagar (Delete).

O PUT se refere a "atualizar", fazer um update dos dados de um usuário na plataforma, o DELETE é para deletar alguns dados relacionados a esse usuário.

Esse acrônimo que mencionamos é o CRUD, base para quando queremos testar, criar uma versão mínima de uma aplicação web.



## 🌐 📡 Protocolo HTTP — Resumo DevOps
🧠 Contexto
Comunicação web acontece através de requisições e respostas
Baseada em:
URLs
DNS
Redes
O HTTP é o protocolo que permite essa comunicação


## 📩 🔄 Estrutura das Mensagens HTTP

As mensagens HTTP possuem estrutura padronizada:

🧱 Partes principais
### 1️⃣ Header (Cabeçalho)
Contém metadados
Exemplo:
Tipo de conteúdo (Content-Type)
Tamanho (Content-Length)
### 2️⃣ Body (Corpo)
Contém os dados enviados
Geralmente em formato JSON


## 📥 📤 Exemplo de Requisição (POST)
```
POST /public/login HTTP/1.1
Content-Type: application/json
Content-length: 42

{"email": "lcs@alura.com", "senha": "123"}
```
### 🔎 Explicação:
POST → método (enviar dados)

/public/login → rota (endpoint)

HTTP/1.1 → versão do protocolo

Body → dados do usuário (JSON)

## 📤 ✅ Exemplo de Resposta
```
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 365

{
  "access_token": "abc123..."
}
```

### 🔎 Explicação:
200 OK → sucesso
Retorna um token de acesso


# 🔑 📌 Métodos HTTP
| Método | Função          |
| ------ | --------------- |
| 'GET'   | Buscar dados    |
| 'POST'   | Enviar dados    |
| 'PUT'    | Atualizar dados |
| 'DELETE' | Remover dados   |

# 📊 📌 Códigos de Status

| Código | Significado        |
| ------ | ------------------ |
| 200    | OK (sucesso)       |
| 400    | Erro na requisição |
| 404    | Não encontrado     |
| 500    | Erro no servidor   |


# 🔗 🔄 Comunicação Cliente x Servidor
```
Cliente (Front-end)
        ↓
   Requisição HTTP
        ↓
Servidor (Back-end)
        ↓
   Resposta HTTP

```

# 🚀 💡 Resumo Final

HTTP é baseado em troca de mensagens estruturadas

Toda requisição possui:

Método

URL

Headers

Body (opcional)

Ferramentas como o Postman facilitam os testes

Métodos HTTP definem o que você quer fazer
