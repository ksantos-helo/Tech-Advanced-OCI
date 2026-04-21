# 🧠📊 Monitoramento no Linux (Resumo DevOps)

## 🔍🔥 Ver processos em tempo real
```bash
top
```

📌 Mostra tudo em execução

🆔 PID = ID do processo

⚙️ CPU / memória em tempo real

🎯 Atalhos dentro do top
U 👤 → filtrar por usuário

F ⚙️ → adicionar/remover colunas

Q ❌ → sair

📋📌 Listar processos
🧾 Lista simples:
```
ps
```

🔎 Lista completa:
```
ps aux
```

👤 USER = usuário

🆔 PID = processo

⚙️ %CPU / %MEM = uso

🔗🔎 Filtrar processos (PIPE + GREP)
📌 Buscar Nginx:
```
ps aux | grep nginx
```

🚫 Remover o próprio grep:
```
ps aux | grep -v grep | grep nginx
```

🔗 | (pipe) = conecta comandos

🔍 grep = busca texto

🚫 -v = exclui resultado

⚡🚀 Forma mais simples (melhor prática)
```
pgrep nginx
```
🎯 Retorna só os PIDs

⚡ Mais direto que grep

🔕🔇 Silenciar saída
📌 Ignorar saída:
```
pgrep nginx > /dev/null
```

📌 Ignorar saída + erro:
```
pgrep nginx &> /dev/null
```

📤 > → redireciona saída

🗑️ /dev/null → “lixeira” do Linux

⚠️ &> → inclui erros

🧪📊 Script de monitoramento (Nginx)
```
#!/bin/bash

if pgrep nginx &> /dev/null
then
  echo "✅ Nginx está operando $(date +"%Y-%m-%d %H:%M:%S")"
else
  echo "❌ Nginx fora de operação $(date +"%Y-%m-%d %H:%M:%S")"
fi
```

▶️⚙️ Executar script
```
chmod +x monitoramento.sh
./monitoramento.sh
```

🔓 chmod +x → permissão de execução

▶️ ./ → executa script

🔄🌐 Controlar Nginx
▶️ Iniciar:
```
sudo service nginx start
```

⛔ Parar:
```
sudo service nginx stop
```

🧠💡 Dicas de DevOps
🧪 pgrep = melhor para scripts

🔇 /dev/null = deixa script limpo

⏱️ date = útil para logs

🔁 automatizar depois com cron

🎯 RESUMÃO FINAL
📊 top → monitoramento em tempo real

📋 ps aux → lista completa

🔍 grep → filtrar processos

⚡ pgrep → forma profissional

🔇 /dev/null → esconder saída

🤖 script bash → automação


---

Se quiser, posso te ajudar a:
- 📁 Organizar isso como um **README profissional no GitHub**
- 🚀 Adicionar badges, estrutura DevOps e deixar nível portfólio
