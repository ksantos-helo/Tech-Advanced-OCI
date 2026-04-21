## 🌐 Comunicação na Web e Modelo TCP/IP (Resumo)

A comunicação entre cliente (usuário) e servidor não depende apenas do HTTP. Na prática, existe uma estrutura mais complexa envolvendo diversos dispositivos de rede (roteadores, modems, switches) e protocolos que trabalham juntos.

---

### 🖧 Redes de Computadores

- Dispositivos intermediários transmitem dados entre cliente e servidor
- Todos precisam seguir **padrões de comunicação**
- Permite conexão entre diferentes dispositivos (celular, notebook, servidores)

---

### 📡 Modelo TCP/IP

A comunicação na rede é organizada em **camadas**, cada uma com uma função específica:

#### 1. Camada de Aplicação
- Onde atua o **HTTP**
- Responsável pela comunicação entre aplicações (ex: navegador e servidor)

#### 2. Camada de Transporte
- Protocolo: **TCP**
- Garante envio confiável dos dados

#### 3. Camada de Rede
- Protocolo: **IP**
- Define endereços de origem e destino (endereços IP)

#### 4. Camadas inferiores (Enlace/Física)
- Responsáveis pela transmissão dos dados pela rede (cabos, roteadores, etc.)

---

### 🔄 Fluxo da Comunicação

1. Cliente envia requisição (HTTP)
2. Dados passam pelas camadas (TCP → IP → rede física)
3. Pacotes trafegam por diversos dispositivos e redes
4. Chegam ao servidor (que processa e responde)
5. Resposta volta pelo mesmo caminho até o cliente

---

### 🌍 Internet

- É uma **rede mundial de computadores** (rede de redes)
- Permite comunicação entre dispositivos em diferentes locais e redes

---

### 🎯 Conclusão

A comunicação entre cliente e servidor envolve múltiplas camadas e protocolos (HTTP, TCP, IP), trabalhando juntos para garantir que os dados cheguem corretamente ao destino.
