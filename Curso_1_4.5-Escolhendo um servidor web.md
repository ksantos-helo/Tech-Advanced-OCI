## Escolhendo um servidor web

✅ Opção mais apropriada: Nginx

## 📌 Por quê?
Porque você tem dois pontos críticos no seu cenário:

Conteúdo predominantemente estático
Alto volume de tráfego

O Nginx foi projetado exatamente para isso.

⚙️ Comparação prática
## 🔹 Nginx (melhor escolha)
Arquitetura assíncrona e orientada a eventos
Consome menos memória
Consegue lidar com milhares de conexões simultâneas
Excelente para:
HTML, CSS, JS
Imagens
APIs leves

👉 Ideal para sites estáticos com muito acesso

## 🔸 Apache
Arquitetura baseada em processos/threads
Consome mais recursos
Melhor para:
Conteúdo dinâmico (PHP tradicional, por exemplo)
Configurações via .htaccess

👉 Pode sofrer mais com alto tráfego simultâneo

## 🧠 Resumo 

👉 O Nginx é mais apropriado, pois sua arquitetura orientada a eventos permite lidar de forma mais eficiente com um grande número de conexões simultâneas, consumindo menos recursos do sistema. Isso o torna ideal para servir conteúdo estático sob alto volume de tráfego.

## 💡 Dica de DevOps (nível profissional)

Em ambientes reais, é comum usar:

Nginx como proxy reverso
Apache ou aplicação backend por trás
