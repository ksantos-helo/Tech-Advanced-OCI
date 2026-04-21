# 🧠 📌 Explicação

Como o HTTP é stateless (sem estado), o servidor não lembra quem é o usuário entre requisições.

##  mecanismo adotado para que o servidor possa reconhecer os usuários entre as requisições de modo eficiente e seguro:

Utilizar cookies para armazenar o identificador de sessão no navegador do usuário.
Cookies são amplamente usados para manter o estado da sessão entre o cliente e o servidor. Ao armazenar o identificador de sessão em um cookie, o navegador do usuário enviará esse identificador a cada nova requisição, permitindo ao servidor reconhecer o usuário.

👉 Para resolver isso, usamos um mecanismo de sessão + identificação.

## 🍪 🔑 Por que cookies são a melhor opção?
Armazenam um ID de sessão no navegador

São enviados automaticamente em cada requisição

Permitem ao servidor:

Identificar o usuário

Manter login ativo

Personalizar a experiência

## 🔄 📡 Como funciona
Usuário faz login

Servidor cria uma sessão

Envia um cookie com ID da sessão

Navegador envia esse cookie em todas as requisições

## ❌ Por que as outras estão erradas?
LocalStorage ❌
→ Não é enviado automaticamente nas requisições (menos seguro)

ID na URL ❌
→ Inseguro (pode vazar facilmente)

Conexão TCP aberta ❌
→ Não é escalável nem viável

Variável global no servidor ❌
→ Não resolve identificação entre requisições de forma correta

## 🎯 ✅ Conclusão

👉 Cookies + sessão são a forma mais eficiente e segura para manter o usuário identificado em aplicações web.
