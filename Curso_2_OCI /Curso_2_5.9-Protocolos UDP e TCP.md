# 📚 TCP vs UDP

## 🌐 Protocolos de Transporte

### ⚡ UDP (User Datagram Protocol)
- **Não orientado à conexão**
- **Rápido**, com baixa latência
- Característica principal:
  - ❌ **Não confiável**
- Não garante:
  - Entrega dos dados
  - Ordem correta
  - Integridade

#### 📌 Uso ideal:
- Streaming de vídeo/áudio
- Jogos online
- Situações onde **velocidade > precisão**

---

### 📦 TCP (Transmission Control Protocol)
- **Orientado à conexão**
- Foco em **confiabilidade**

#### 🔒 Garantias:
- ✔️ Entrega dos dados
- ✔️ Ordem correta
- ✔️ Integridade

#### 🔄 Funcionamento:
- Utiliza o **three-way handshake**:
  1. SYN
  2. SYN-ACK
  3. ACK

👉 Esse processo estabelece uma conexão segura antes da transmissão.

---

## ⚖️ Comparação Geral

| Característica   | TCP                     | UDP                    |
|-----------------|-------------------------|------------------------|
| Conexão         | Orientado à conexão     | Não orientado          |
| Confiabilidade  | Alta                    | Baixa                  |
| Velocidade      | Mais lento              | Mais rápido            |
| Ordem dos dados | Garantida               | Não garantida          |

---

## 🧠 Conclusão
- **TCP** → ideal quando a **confiabilidade é essencial** (ex: web, APIs).
- **UDP** → ideal quando a **velocidade é prioridade** (ex: streaming).

[ artigo: (O que é UDP e TCP? Entenda quais as diferenças e como funciona cada Protocolo).](https://www.alura.com.br/artigos/quais-as-diferencas-entre-o-tcp-e-o-udp)
