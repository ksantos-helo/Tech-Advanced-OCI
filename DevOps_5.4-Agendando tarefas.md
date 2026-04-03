# ⏱️🤖 Agendamento de Tarefas com Cron (DevOps - Linux)

## 🧠 📌 Objetivo
Automatizar a execução de um script de monitoramento do **Nginx**, salvando logs em um arquivo para análise.

---

## ⚙️ 🔧 Instalando o cron

```bash
sudo apt-get update
sudo apt-get install cron
```

📦 Atualiza pacotes

⏱️ Instala o serviço de agendamento

📝 ✏️ Editando o crontab
```
crontab -e
```

🧾 Abre o editor (nano)

📅 Permite agendar tarefas automáticas

🧩 📊 Estrutura do crontab
```
* * * * * comando
│ │ │ │ │
│ │ │ │ └── dia da semana
│ │ │ └──── mês
│ │ └────── dia do mês
│ └──────── hora
└────────── minuto
```

🎯 Exemplo:
```
* * * * *
```

👉 Executa a cada minuto

📁 📄 Criando arquivo de log
```
touch /home/usuario/saida_nginx.txt
```

📌 Arquivo onde será salvo o resultado do script

🤖 🚀 Agendando o script
```
* * * * * /home/usuario/monitoramento.sh >> /home/usuario/saida_nginx.txt
```

🔁 Executa a cada minuto

📤 >> adiciona saída ao arquivo

🧾 Gera histórico (logs)

📊 🔍 Verificando logs
```
cat /home/usuario/saida_nginx.txt
```

🧾 Exemplo de saída:
```
Nginx esta operando 2023-11-23 13:28:01
Nginx esta operando 2023-11-23 13:29:01
```

⏱️ Mostra data e hora

✅ Indica status do servidor

🧠 💡 Boas práticas DevOps
🔁 Automatizar tarefas com cron

🧾 Sempre gerar logs

⏱️ Usar timestamp (date)

🔍 Monitorar serviços críticos (Nginx, APIs, etc.)

🎯 🚀 Resumo Final
⚙️ cron → agenda tarefas automáticas

📝 crontab -e → configura agendamento

🔁 * * * * * → executa a cada minuto

📤 >> → salva logs

📊 monitoramento contínuo = prática DevOps essencial

🔥 Próximo passo (nível profissional)
⏱️ Automatizar com alertas

📊 Integrar com Grafana/Prometheus

☁️ Monitorar em cloud (AWS, OCI, Azure)
