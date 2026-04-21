## Atividades

### 1️⃣ Elabore um script que automatiza a atualização de pacotes do sistema operacional.

```
#!/bin/bash
sudo apt update -y
sudo apt upgrade -y
```

O script utiliza os comandos apt update e apt upgrade para automatizar a atualização de pacotes no sistema operacional Debian/Ubuntu. O parâmetro -y é usado para confirmar automaticamente todas as perguntas de confirmação.

### 2️⃣ Crie um script que renomeie todos os arquivos em um diretório, adicionando um prefixo ou sufixo especificado.
```
#!/bin/bash
prefixo="Novo_"
for arquivo in *; do
  mv "$arquivo" "$prefixo$arquivo"
done
```
O script adiciona o prefixo "Novo_" aos nomes de todos os arquivos no diretório em que é executado.


### 3️⃣Desenvolva um script que automatiza a criação de usuários no sistema, solicitando ao usuário que forneça o nome e outros detalhes necessários.
```
#!/bin/bash
echo "Digite o nome do novo usuário:"
read nome_usuario
sudo useradd -m $nome_usuario
sudo passwd $nome_usuario
```
O script solicita ao usuário o nome do novo usuário, cria um diretório pessoal para o usuário (useradd -m), e define uma senha (passwd).

### 4️⃣Construa um script para monitorar o espaço em disco usando o comando df na coleta de informações.

```
#!/bin/bash
limite=90
espaco=$(df -h | awk 'NR==2 {print $5}' | sed 's/%//')

if [ $espaco -gt $limite ]; then
  echo "Alerta: Espaço em disco excedeu $limite%."
else
  echo "Espaço em disco está abaixo do limite."
fi
```
O script coleta a porcentagem de espaço em disco usando o comando df, compara com um limite predefinido (90% neste exemplo) e emite um alerta se exceder.

### 5️⃣ Escreva um script para automatizar o backup de um diretório específico para um local de destino, utilizando a compressão gzip.

```
#!/bin/bash
origem="/caminho/do/diretorio"
destino="/caminho/do/backup"
data=$(date +"%Y%m%d")
tar -czf $destino/backup_$data.tar.gz $origem
```
O script utiliza o comando tar para criar um arquivo compactado e tarball, adicionando a data ao nome do arquivo para distinguir backups diários. O gzip (-z) é usado para compressão.
