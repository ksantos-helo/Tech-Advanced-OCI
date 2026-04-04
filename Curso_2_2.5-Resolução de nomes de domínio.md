# 🌐 DNS e Resolução de Nomes

A conversão de **nomes de domínio** (ex: `alura.com.br`) em **endereços IP** é feita pelos **servidores DNS**.

Quando acessamos um site:
- Nosso dispositivo 📱💻 envia uma consulta ao **DNS configurado na rede**
- O DNS tenta encontrar o IP correspondente ao domínio

---

## ❓ Pergunta
O que acontece quando o servidor DNS **não possui o IP em cache**?

---

## ✅ Resposta: Resolução DNS (passo a passo)

Quando o DNS local não encontra o IP, ele inicia uma **busca hierárquica**:

### 1️⃣ Servidor Raiz 🌳
- O DNS consulta os **servidores raiz**
- Eles indicam qual servidor gerencia o **TLD**
- Exemplo: `.com`, `.br`

---

### 2️⃣ Servidor TLD 🔝
- O DNS consulta o servidor do domínio de topo
- Ele informa qual é o **servidor autoritativo** do domínio

---

### 3️⃣ Servidor Autoritativo 📡
- Possui o **IP real do domínio**
- Exemplo:
alura.com.br → 172.67.72.232


---

### 4️⃣ Retorno ao Cliente 🔑
- O DNS local:
- Recebe o IP
- Armazena no **cache** 🗂️
- Retorna ao dispositivo
- O cliente acessa o servidor corretamente 🌍

---

## 🧠 Resumo Final
- Se o DNS não sabe o IP:
DNS Local → Raiz → TLD → Autoritativo → IP → Cliente

- Processo garante:
- 📍 Localização correta do servidor
- ⚡ Melhor desempenho (cache)
- 🌐 Funcionamento da navegação na internet
