# 🔐🌐 HTTPS e Criptografia — Resumo

- HTTPS utiliza **criptografia assimétrica + simétrica**

---

## 🔑 Criptografia Assimétrica
- Usa **duas chaves**:
  - 🔓 Pública → criptografar
  - 🔒 Privada → descriptografar
- ✔️ Mais segura  
- ❌ Mais lenta  

👉 Exemplo:
- Navegador usa a **chave pública**
- Servidor usa a **chave privada**

---

## 🔐 Criptografia Simétrica
- Usa **uma única chave**
- ✔️ Muito mais rápida  
- ❌ Menos segura isoladamente  

---

## 🔄 Como o HTTPS funciona

1️⃣ Início da conexão:
- Usa **criptografia assimétrica**
- Cliente recebe chave pública do servidor  

2️⃣ Criação da chave de sessão:
- Cliente gera uma **chave simétrica**
- Envia de forma segura (assimétrica)

3️⃣ Comunicação contínua:
- Usa **criptografia simétrica**
- Mais rápida e eficiente  

---

## 🎯 Conclusão
- HTTPS combina:
  - 🔒 Segurança (assimétrica)
  - ⚡ Performance (simétrica)
- Garante comunicação segura e eficiente 🚀
