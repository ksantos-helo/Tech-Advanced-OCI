# 🧠 Resumo – Shell Script, Automação e Tar

## 💻 Interface de Linha de Comando
- Mais eficiente que interface gráfica em servidores  
- Facilita acesso, configuração e manutenção  
- Padrão em ambientes Linux  

---

## ⚙️ Automação de tarefas
- Evita executar comandos manualmente repetidamente  
- Usamos scripts (Shell Script) para automatizar  
- Script = “roteiro de comandos”  

---

## 📜 Estrutura básica de um script
```bash
#!/bin/bash
```

Define o interpretador (Bash)

📦 Exemplo: Script de backup
Variáveis
```
diretorio="/caminho"
nome_arquivo="backup_$(date +%Y%m%d_%H%M%S).tar.gz"
```

date gera data/hora automática no nome

Compactação com tar
```
tar -czf "$nome_arquivo" "$diretorio"
```

c → criar

z → compactar (gzip)

f → nome do arquivo

Mensagem
```
echo "Backup concluído em $nome_arquivo"
```

🔐 Permissão e execução
```
chmod +x script.sh
./script.sh
```

🔁 Parâmetros em scripts
$1, $2 → argumentos

$@ → todos argumentos

$# → quantidade de argumentos

✅ Validação com if
```
if [ "$#" -lt 2 ]; then
  echo "Erro: parâmetros insuficientes"
  exit 1
fi
```

📂 Separar parâmetros
```
arquivo_saida="$1"
arquivos=("${@:2}")
```

📦 Compactação com parâmetros
```
tar -czf "$arquivo_saida" "${arquivos[@]}"
```

🧪 Verificar conteúdo do .tar
```
tar -tf arquivo.tar.gz
```

🔎 Condicionais no Bash

Estrutura
```
if [ condição ]; then
  comandos
elif [ outra ]; then
  comandos
else
  comandos
fi
```

Operadores importantes
🔤 Strings
= → igual

!= → diferente

🔢 Números
-eq → igual

-ne → diferente

-gt → maior

-lt → menor

-ge → maior ou igual

📁 Arquivos
-e → existe

💡 Boas práticas
Sempre usar aspas " "

Cuidar dos espaços no [ ]

Validar parâmetros

Automatizar tarefas repetitivas

🎯 Ideia principal
Scripts Bash = automação + produtividade + padronização no Linux
