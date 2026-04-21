# 🕵️‍♂️📡 Wireshark — Resumo Prático

## ▶️ Captura de tráfego
- 🔌 Selecionar: **Adapter for loopback traffic capture**
- 📡 Inicia captura de pacotes da rede

---

## 🔍 Filtro para HTTP
- Usar filtro:
```
bash
tcp.port == 8000 && http
```

👉 Filtra apenas tráfego HTTP na porta 8000

## 🧪 Teste com requisição (Postman)
POST http://localhost:8000/public/login
```
{
  "email": "lcs@alura.com",
  "senha": "123"
}
```
📤 Envia requisição
🔑 Recebe token de acesso

## ⚠️ Problema identificado
Wireshark mostra:

📧 Email

🔑 Senha

❌ Dados visíveis na rede (HTTP não é seguro)

## 🔐 Solução: HTTPS

🔒 Usa criptografia (SSL/TLS)

🛡️ Protege os dados trafegados

🌐 Evita exposição de informações sensíveis

## 🎯 Resumo final

HTTP → dados visíveis ❌

HTTPS → dados protegidos ✅
