# Coletando métricas do Nginx

>>> Você precisa se certificar de que o servidor está operando dentro de sua capacidade e não sobrecarregado. Considerando esse cenário, é necessário criar um script para monitorar as métricas de conexões ativas e requisições por segundo.

Sabendo que a URL “http://localhost/nginx_status” permite acesso ao status do servidor Nginx e o comando curl é usado como ferramenta para fazer solicitações HTTP e coletar informações de URLs.

Qual script você faria para coletar essas métricas?

✅ ✔️ Script correto

```
#!/bin/bash

get_nginx() {
  local metrics=$(curl -s "http://localhost/nginx_status")
  if [[ -n "$metrics" ]]; then
    local active_connections=$(awk 'NR==1 {print $3}' <<< "$metrics")
    local requests_per_second=$(awk 'NR==3 {print $2}' <<< "$metrics")
    echo "Active connections: $active_connections"
    echo "Requests per second: $requests_per_second"
  else
    echo "Failure in collecting Nginx metrics."
  fi
}

get_nginx
```

## 🧠 💡 Por que essa é a correta?
✅ Usa as ferramentas certas:

🌐 curl → coleta dados da URL

🔍 awk → extrai informações específicas

⚙️ função organizada (get_nginx)

## ✅ O que o script faz corretamente:
📡 Acessa: http://localhost/nginx_status

📊 Extrai:

🔗 Active connections (linha 1)

📈 Requests per second (linha 3)

⚠️ Trata erro se não houver retorno
