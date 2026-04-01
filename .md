# 🧠💻 Monitoramento de Memória com Script (Linux + DevOps)

## 🎯 📌 Objetivo
Identificar os 15 processos que mais consomem memória
Executar automaticamente a cada 5 minutos
Salvar os resultados em um arquivo de log
⚙️ 🧪 Script completo
```
#!/bin/bash

# Arquivo de saída com data e hora
output_file="/home/usuario/top_processes_$(date +%Y%m%d_%H%M).txt"

# Listar processos e salvar os 15 maiores consumidores de memória
ps -e -o pid,%mem --sort=-%mem | head -n 16 > "$output_file"
```

## 🔍 📊 Explicação dos comandos
🧾 ps
```
ps -e -o pid,%mem --sort=-%mem
```
-e → mostra todos os processos
-o pid,%mem → mostra:
🆔 PID (processo)
💾 %MEM (uso de memória)
--sort=-%mem → ordena do maior para o menor
## 🔗 |
```
| head -n 16
```

🔗 Pipe → envia saída de um comando para outro
📊 head -n 16:
Mostra as 16 primeiras linhas
(1 cabeçalho + 15 processos)
## 📤 >
```
> "$output_file"
```

📁 Salva o resultado no arquivo
🧾 Sobrescreve o conteúdo anterior
## 🕒 date
```
$(date +%Y%m%d_%H%M)
```

## 📅 Gera data e hora no nome do arquivo
Exemplo:
```
top_processes_20260331_1430.txt
```


👉 Isso evita sobrescrever logs (boas práticas DevOps)

# 🤖 ⏱️ Automatizando com cron
📌 Editar crontab:
```
crontab -e
```

🚀 Agendamento a cada 5 minutos:
```
*/5 * * * * /home/usuario/seu_script.sh
```

## 🧠 💡 O que esse cron faz?
*/5 → executa a cada 5 minutos
📊 coleta dados automaticamente
📁 gera logs contínuos
📊 📁 Resultado esperado

Arquivos sendo criados automaticamente:
```
top_processes_20260331_1400.txt
top_processes_20260331_1405.txt
top_processes_20260331_1410.txt
```

Cada um contendo:
```
PID   %MEM
1234  12.5
5678  10.2
```

## 🚀 💡 Boas práticas DevOps
📊 Monitorar recursos constantemente

🧾 Gerar logs com timestamp

🤖 Automatizar com cron

🔍 Usar ps + sort + head para análise rápida

## 🎯 🔥 Resumo final
🧾 ps → lista processos

📊 --sort=-%mem → ordena por memória

🔗 | head → pega os principais

📁 > → salva em arquivo

⏱️ cron → automatiza execução
