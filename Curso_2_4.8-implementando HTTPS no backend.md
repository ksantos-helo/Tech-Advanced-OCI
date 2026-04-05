# 🔐🚀 Implementando HTTPS no Back-end — Passo a Passo

###  🧰 Pré-requisito
- ✔️ Ter o **OpenSSL** instalado

---

### 1️⃣ Acessar o projeto
```bash
cd api-alurabooks
```

### 2️⃣ Gerar chave e certificado
```
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout server.key -out server.crt
```

### 📁 Arquivos criados:

🔑 server.key → chave privada

📜 server.crt → certificado digital

### 3️⃣ Abrir o projeto no editor
💻 Abrir no VS Code (ou outro editor)

### 4️⃣ Importar HTTPS
No arquivo server.js, adicionar no topo:
```
const https = require("https")
```

### 5️⃣ Configurar servidor HTTPS
Substituir a parte do listen por:
```
https.createServer({
  key: fs.readFileSync('server.key'),
  cert: fs.readFileSync('server.crt')
}, server).listen(8000, () => {
  console.log("API disponível em https://localhost:8000")
})
```

### 6️⃣ Salvar e reiniciar o servidor
```
npm run start-auth
```

### 🎯 Resultado
🔒 Aplicação agora usa HTTPS

🛡️ Comunicação criptografada

🚀 Mais segurança para dados sensíveis

