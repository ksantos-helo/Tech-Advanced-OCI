# Projeto AllBooks – Conceitos de Acesso Web

# Projeto AllBooks – Conceitos de Acesso Web

| Conceito      | O que é / Função                                    | Exemplo                        |
|---------------|-----------------------------------------------------|--------------------------------|
| **URL**       | Localiza recursos na web (páginas, scripts, serviços) | http://localhost:3000/         |
| **Protocolo** | Define tipo de comunicação                          | HTTP, HTTPS, FTP, SSH          |
| **Servidor**  | Endereço ou nome que identifica o computador/servidor | localhost, google.com.br       |
| **Porta**     | Permite múltiplos serviços no mesmo servidor       | Front-end: 3000 <br> Back-end: 8000 <br> HTTPS: 443 |
| **Caminho**   | Indica qual recurso acessar dentro do servidor     | `/` → raiz/Home                |
| **IP**        | Endereço único do servidor na rede                 | 192.168.0.1                    |
| **DNS**       | Mapeia nomes amigáveis para IPs                     | google.com.br → 142.250.190.78 |



## 1. URL (Uniform Resource Locator)
- Localiza recursos na web: páginas, scripts, serviços.
- Estrutura básica:  
protocolo://servidor:porta/caminho

- **Protocolo:** tipo de comunicação (HTTP, HTTPS, FTP, SSH)  
- **Servidor:** endereço ou nome do servidor (`localhost`, domínio)  
- **Porta:** conecta a um serviço específico (ex: 3000, 8000)  
- **Caminho:** recurso dentro do servidor (`/` → raiz/Home)

---

## 2. Porta
- Permite múltiplos serviços em um mesmo dispositivo.
- Portas padrão: 0–1022  
- Portas livres (desenvolvimento): 1023–65535  
- Exemplo:  
- Front-end: 3000  
- Back-end: 8000  
- Google HTTPS: 443 (padrão, não precisa informar)

---

## 3. Servidor e IP
- Servidores possuem **endereços IP únicos** para localização na rede.
- Para facilitar, usamos **nomes amigáveis** mapeados para IPs via **DNS**.

---

**Resumo:**  
- **URL** → localiza recurso  
- **Protocolo** → define tipo de comunicação  
- **Porta** → identifica serviço no servidor  
- **Servidor/IP** → localiza fisicamente o recurso  
- **DNS** → mapeia nomes amigáveis para IPs
