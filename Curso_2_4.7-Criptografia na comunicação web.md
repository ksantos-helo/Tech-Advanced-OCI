# 🔐🌐 HTTPS, Certificado e Chaves — Resumo

- HTTPS garante **confidencialidade** dos dados na comunicação cliente ↔ servidor  
- Utiliza **criptografia** para tornar os dados ilegíveis na rede  

---

## 📁 Arquivos importantes

### 📜 server.crt (Certificado Digital)
- Representa a **identidade do servidor**
- Contém:
  - 🌍 País, organização
  - 🔑 Chave pública
  - ✍️ Assinatura digital

### 🔑 server.key (Chave Privada)
- Fica **apenas no servidor**
- Usada para **descriptografar os dados**
- Exemplo: chave RSA de 2048 bits

---

## 🛠️ Comandos OpenSSL

### Ver certificado:
```
bash
openssl x509 -in server.crt -text
```
Ver chave privada:
```
openssl rsa -in server.key -text -noout
```
### 🔄 Como funciona na prática
🔓 Servidor envia o certificado (chave pública)

📤 Cliente usa essa chave para criptografar dados

📥 Servidor usa a chave privada para descriptografar

### 🔐 Tipo de criptografia
Assimétrica:

🔑 Chave pública → criptografa

🔒 Chave privada → descriptografa

### 🎯 Conclusão
HTTPS usa TLS/SSL + criptografia assimétrica

Garante segurança na troca de dados

Protege informações sensíveis (senha, email, etc.) 🚀
