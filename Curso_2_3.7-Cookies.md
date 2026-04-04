# 🌐📡 Resumo — HTTP Stateless e Cookies

## 🧠 Conceito de 'Stateless'
- Aplicações web são **stateless (sem estado)**
- Cada requisição HTTP é:
  - Independente
  - Não guarda informações anteriores

---

## ⚠️ Limitação dos servidores HTTP
- Não armazenam dados do cliente automaticamente
- Não mantêm o usuário logado
- Não identificam se requisições são do mesmo usuário

---

## 🍪 🔑 Solução: Cookies

### 📥 Como funciona

1. Primeira requisição:
   - Servidor envia um header:
```
http
   Set-Cookie
```
Dados são armazenados no navegador

Próximas requisições:

Navegador envia de volta:
```
Cookie
```
Servidor reconhece o usuário

### 🔄 Fluxo resumido
```
Cliente → Requisição → Servidor
Servidor → Set-Cookie → Cliente
Cliente → Cookie → Servidor
```

### 🎯 Função dos Cookies
Identificar usuários

Manter sessões (login)

Personalizar experiência

### 🚀 Resumo final
HTTP não mantém estado

Cookies resolvem esse problema

Funcionam via headers (Set-Cookie e Cookie)

[O que são Cookies na Internet e como eles funcionam?](https://www.alura.com.br/artigos/o-que-sao-cookies-como-funcionam)
