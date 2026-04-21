## 🔗 Modelo Cliente-Servidor vs Peer-to-Peer (P2P)

### 🖥️ Modelo Cliente-Servidor

- Baseado na divisão entre:
  - **Cliente:** solicita recursos/serviços
  - **Servidor:** fornece recursos/serviços
- O cliente **não compartilha recursos**, apenas faz requisições
- O servidor fica em **modo de escuta**, aguardando solicitações

### ⚠️ Limitações

- **Centralização** no servidor
- Pode ocorrer:
  - Sobrecarga
  - Falhas
  - Indisponibilidade

📌 Exemplo: sites de venda de ingressos com muitos acessos simultâneos

### 🚀 Soluções comuns

- Escalabilidade
- Balanceamento de carga
- Redundância

---

### 🔄 Modelo Peer-to-Peer (P2P)

- Arquitetura **descentralizada**
- Cada dispositivo pode atuar como:
  - Cliente
  - Servidor
- Compartilhamento direto de recursos (sem intermediários)

### ✅ Vantagens

- Maior escalabilidade
- Maior resistência a falhas
- Redundância natural

---

### 💡 Exemplos

- Compartilhamento de arquivos (BitTorrent)
- Criptomoedas (Bitcoin / blockchain)

---

### 🎯 Resumo

- **Cliente-Servidor:** centralizado, mais controle, porém mais vulnerável a falhas
- **P2P:** descentralizado, mais resiliente e escalável
