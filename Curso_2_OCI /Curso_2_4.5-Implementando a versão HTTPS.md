# 🔐🌐 HTTPS com OpenSSL — Resumo para Estudos

## ⚠️ Problema
- HTTP ❌ → dados trafegam sem segurança
- Informações (email, senha) podem ser capturadas

---

## 🔒 Solução
- Implementar **HTTPS (TLS/SSL)**
- Criptografar comunicação cliente ↔ servidor

---

## 🛠️ Geração de chave e certificado (OpenSSL)

```
bash
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout server.key -out server.crt
```

## 📁 Arquivos gerados:
🔑 server.key → chave privada

📜 server.crt → certificado digital

## 💻 Implementação no servidor (Node.js)
Importar HTTPS:
```
const https = require('https')
```

Configurar servidor seguro:
```
https.createServer({
  key: fs.readFileSync('server.key'),
  cert: fs.readFileSync('server.crt')
}, server).listen(8000, () => {
  console.log("API disponível em https://localhost:8000")
})
```

## ▶️ Executar servidor
```
npm run start-auth
```

## 🧪 Teste com Postman
```
POST https://localhost:8000/public/login
```
-----
```
{
  "email": "lcs@alura.com",
  "senha": "123"
}
```

## 🕵️‍♂️ Teste no Wireshark
Filtro:
```
tcp.port == 8000 && tls
```

## 🔍 Resultado:
❌ HTTP → dados visíveis

✅ HTTPS → dados criptografados (ilegíveis)

## 🎯 Conclusão
HTTPS protege dados com criptografia 🔒

TLS impede leitura de informações sensíveis 🛡️

Essencial para segurança em aplicações web 🚀
