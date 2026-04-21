# 📚 Resumo para Estudos: Evolução do HTTP e Protocolos de Transporte

## 🔐 Evolução da Segurança na Web
- O **SSL (Secure Sockets Layer)** evoluiu ao longo do tempo, mas apresentou vulnerabilidades.
- Foi substituído pelo **TLS (Transport Layer Security)**, mais seguro e amplamente usado atualmente.
- O mesmo processo evolutivo ocorreu com o protocolo **HTTP**.

---

## 🌐 Versões do HTTP

### 🔹 HTTP/1.1
- Comunicação baseada em **requisições sequenciais**.
- Para melhorar desempenho:
  - Uso de **múltiplas conexões paralelas**.
- Problema:
  - **Gargalo** devido ao excesso de conexões.
- Modelo:
  - **Cliente sempre inicia** a comunicação (request → response).

---

### 🔹 HTTP/2
- Criado para resolver limitações do HTTP/1.1.

#### Principais melhorias:
- **Multiplexação**:
  - Várias requisições em **uma única conexão TCP**.
- **Cabeçalhos otimizados**:
  - Menores → melhor desempenho.
- **Server Push**:
  - Servidor envia dados **proativamente**, sem requisição explícita.
- **Segurança integrada** (uso comum com TLS).

---

### 🔹 HTTP/3
- Baseado no protocolo **QUIC** (não usa TCP).
- Representa uma evolução significativa em desempenho e segurança.

#### Principais características:
- Utiliza **UDP** como base (mais rápido que TCP).
- **QUIC**:
  - Compensa perdas de pacotes com múltiplos fluxos.
  - **Criptografia embutida** (inclui TLS).
- Elimina o **three-way handshake** do TCP.
- Comunicação mais **rápida e eficiente**.

---

## 🔄 TCP vs UDP

### 📦 TCP (Transmission Control Protocol)
- **Confiável** (garante entrega dos dados).
- Usa o **three-way handshake**.
- Mais lento devido às validações.

### ⚡ UDP (User Datagram Protocol)
- **Mais rápido**, porém:
  - Não garante entrega dos dados.
- Ideal para:
  - **Streaming de vídeo**
  - Situações onde pequenas perdas não impactam muito.

---

## ⚙️ HTTP/3 vs HTTP/1.1 e HTTP/2

| Característica        | HTTP/1.1 & HTTP/2        | HTTP/3 (QUIC)              |
|----------------------|--------------------------|----------------------------|
| Protocolo base       | TCP                      | UDP (via QUIC)             |
| Segurança            | TLS separado             | Criptografia embutida      |
| Conexão inicial      | Lenta (handshake TCP + TLS) | Rápida (sem handshake TCP) |
| Performance          | Boa (melhor no HTTP/2)   | Superior                   |

---

## 🚀 Conclusão
- O **HTTP/3** traz:
  - Maior **velocidade**
  - Melhor **segurança**
- Ainda está em **adoção gradual** (nem todas as ferramentas suportam totalmente).
- A evolução contínua dos protocolos é essencial para:
  - Melhorar **performance**
  - Garantir **segurança**
- Faz parte das boas práticas do **DevOps** manter sistemas atualizados.

---
