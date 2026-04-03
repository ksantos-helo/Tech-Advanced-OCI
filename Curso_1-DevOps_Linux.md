# 🐧 Linux Server via SSH – Resumo

## 💻 Prompt de comando
Exemplo:
lucasrm@lucaspc:~$

- 👤 lucasrm: usuário  
- 🖥️ lucaspc: nome da máquina  
- 📁 ~: diretório home  
- 💲 $: usuário comum (sem privilégios administrativos)

---

## 🔄 Atualizações do sistema
sudo apt update
- 🔐 sudo: executa como administrador  
- 📦 apt: gerenciador de pacotes  
- 🔍 update: verifica atualizações disponíveis  

---

## 🧠 Shell CLI
- Interface de linha de comando  
- Executa apenas comandos válidos  
- Muito usada em servidores  

---

## 📁 Navegação e diretórios

### 📍 Ver diretório atual
pwd

### 📂 Listar arquivos
ls
ls -a # inclui ocultos
ls -l # detalhado


### ❓ Ajuda
ls --help


---

## 📂 Criar diretórios

mkdir devops


---

## 🚶 Navegar entre diretórios

cd devops # entrar
cd .. # voltar
cd ~ # home
cd # também vai para home

history

- ⬆️⬇️ também navegam no histórico

---

## 📄 Criar arquivos

touch notas.txt


---

## ✏️ Manipulação de arquivos

### 📝 Inserir conteúdo

cat > notas.txt

- Digitar conteúdo  
- ⌨️ Ctrl + D para sair  

### 👀 Visualizar

cat notas.txt


---

## 📢 Comando echo

echo "texto"
echo "texto" > arquivo.txt

- ⚠️ `>` sobrescreve o conteúdo

---

## 🧾 Editor nano

### 📥 Instalar

sudo apt-get install nano


### ✍️ Usar

nano arquivo.txt

- ❌ Ctrl + X: sair  
- 💾 Y: salvar  

---

## 📦 Compactação

tar -czf arquivo.tar.gz arquivo1 arquivo2


---

## 🚚 Movimentação

mv arquivo destino/


---

## ❌ Remoção

### 🗑️ Arquivo

rm arquivo.txt


### 📁 Diretório vazio

rmdir pasta


### ⚠️ Diretório com conteúdo

rm -r pasta


- ❗ Exclusão é permanente

---

## 🌳 Estrutura de diretórios
- Organização em árvore  
- Exemplo:

/home/usuario/devops


---

## 🎯 Conceitos principais
- 💻 Uso via terminal  
- 🚫 Sem interface gráfica  
- ⚙️ Mais controle e eficiência  
- 🌐 Muito usado em produção e DevOps 




