## 🧠 📌 Conceito geral

Você está trabalhando com duas partes:

### 🔙 Back-end

👉 Responsável por:

Processar dados
Autenticação (login, segurança)
APIs
### 🎨 Front-end

👉 Responsável por:

Interface visual
Interação com usuário
Consome a API do back-end

## 🔙 ⚙️ BACK-END (API)
📁 Entrar na pasta do back-end
```
cd api-alurabooks
```

👉 Isso te leva para a pasta onde está a API

▶️ Rodar o servidor back-end
```
npm run start-auth
```

👉 Esse comando:

Inicia o servidor
Ativa autenticação (login, token, etc.)
Deixa a API disponível (geralmente em algo como http://localhost:3000)

🧠 O que está acontecendo aqui?
Você está subindo uma API
O Postman pode ser usado aqui para testar os endpoints

## 🎨 💻 FRONT-END (React)
📁 Entrar na pasta do front-end
```
cd curso-react-alurabooks
```

👉 Agora você está no projeto visual

▶️ Rodar o front-end
```
npm start
```

👉 Esse comando:

Inicia o projeto React
Abre no navegador (ex: http://localhost:3000 ou 3001)
Mostra a interface do sistema
🧠 O que acontece aqui?
O front faz requisições para o back-end
Exemplo:
Front → pede dados
Back → responde via API

### 🔗 🔄 Como os dois se conectam
```
[ Front-end (React) ]  →  faz requisição  →  [ Back-end (API) ]
                              ↑
                         responde dados
```

## ⚠️ Dica MUITO importante

👉 Você precisa deixar os dois rodando ao mesmo tempo

Abra 2 terminais:

### Terminal 1 (Back-end)
```
cd api-alurabooks
npm run start-auth
```

### Terminal 2 (Front-end)
```
cd curso-react-alurabooks
npm start
```

## 🚀 Resumo rápido (pra GitHub ou revisão)
### 🔙 Back-end
cd api-alurabooks

npm run start-auth

👉 Sobe a API

### 🎨 Front-end
cd curso-react-alurabooks

npm start

👉 Abre a interface
