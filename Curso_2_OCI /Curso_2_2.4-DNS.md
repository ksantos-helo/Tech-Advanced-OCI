# 🌐 Como funcionam os endereços amigáveis e o DNS


# 🌐 Resumo: Endereços, IP e DNS

| Conceito      | Função / Explicação                                       | Exemplo / Observação                       |
|---------------|-----------------------------------------------------------|-------------------------------------------|
| 🌐 Endereço amigável | Facilita o acesso a sites digitáveis | `alura.com.br` 🖥️ |
| 🆔 IP        | Identifica unicamente cada dispositivo na rede           | `172.67.72.232` 🌍 |
| 📡 Ping      | Testa conectividade com um servidor                      | `ping alura.com.br` → responde com IP ✅ |
| 🛤️ Traceroute | Mostra o caminho que os pacotes percorrem até o servidor | Saltos entre dispositivos até o destino |
| 🔄 DNS       | Tradução de nomes de domínio em IPs                     | Nome amigável → IP do servidor            |
| 🌳 Servidor raiz | Início da resolução DNS                                | Direciona para TLD                         |
| 🔝 TLD       | Domínio de nível superior (.com, .br, .org, .net)       | `.com`, `.br`                              |
| 📡 Servidor autoritativo | Possui mapeamento correto do domínio para IP | `alura.com.br` → `172.67.72.232`         |
| 🔑 Cliente   | Recebe IP do DNS e acessa o servidor                     | Navegador conecta ao site                  |


## 1️⃣ Endereços amigáveis x Endereços IP
- Usamos **endereços amigáveis** para acessar sites facilmente, ex: `alura.com.br` 🖥️  
- Cada dispositivo tem um **IP único** 🌍  
- Teste de conectividade com `ping`:
  ```bash
  C:\> ping alura.com.br
  Resposta de 172.67.72.232: bytes=32 tempo=1ms TTL=59
O endereço amigável mapeia para um IP para enviar mensagens ao servidor correto 🔗

## 2️⃣ Rastreando a rota até o servidor
Com traceroute ou tracert podemos ver o caminho dos pacotes 🛤️

Os pacotes passam por múltiplos dispositivos (saltos) até chegar ao servidor final

Exemplo: Alura → IP 172.67.72.232 ✅

## 3️⃣ Sistema DNS (Domain Name System)
O DNS traduz nomes de domínio em IPs 🔄

Passo a passo:

Cliente digita alura.com.br ✏️

Servidor DNS local verifica cache 🗂️

Se não encontrar, consulta servidor raiz 🌳

Servidor raiz retorna TLD (Top-Level Domain, ex: .com, .br) 🔝

Servidor autoritativo responde com o IP correto 📡

Cliente recebe IP e acessa o servidor 🔑

## 4️⃣ Hierarquia do DNS
Estrutura hierárquica:

Raiz → TLDs (.com, .br, .org, .net) → domínios específicos (alura, fiap, g1) 🏛️

Facilita localização e administração dos domínios ⚙️

## 5️⃣ Próximo passo
Entender como HTTP utiliza esse mapeamento para comunicação entre cliente e servidor 📤📥

