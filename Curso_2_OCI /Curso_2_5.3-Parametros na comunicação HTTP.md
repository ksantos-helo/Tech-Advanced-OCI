# Envio de Parâmetros e Requisições no Projeto AllBooks

## 1. Acesso ao Front-end
No front-end do projeto AllBooks (localhost:3000), há categorias populares:
- Android
- Orientação a Objetos
- Marketing Digital
- Agile
- Startups
- HTML & CSS
- Java
- Python

Deseja-se enviar um parâmetro ao clicar em uma categoria para requisitar livros específicos do back-end.

---

## 2. Requisições via Postman

### 2.1 Método GET
- URL base para livros: `https://localhost:8000/livros`
- Para buscar livros de uma categoria específica, utilizamos **Query Parameters** na URL:
  ```text
  https://localhost:8000/livros?categoria=1
  
Ao clicar em "Send", recebemos um JSON com todos os livros daquela categoria.

Exemplo de retorno JSON parcial:
  ```
{
  "id": 1,
  "titulo": "Acessibilidade na Web",
  "slug": "acessibilidade-na-web",
  "categoria": 3,
  "descricao": "Boas práticas para construir sites e aplicações acessíveis",
  "isbn": "978-65-86110-10-4",
  "numeroPaginas": 246,
  "publicacao": "2020-04-01",
  "imagemCapa": "https://raw.githubusercontent.com/viniciosneves/alurabooks/curso-novo/public/imagens/livros/acessibilidade.png",
  "autor": 1,
  "opcoesCompra": [...]
}
  ```
2.2 Método POST
Utilizado para inserir novos livros, não sendo viável passar dados pela URL.

URL: https://localhost:8000/livros

Corpo da requisição: JSON com os dados do livro.

Exemplo JSON para cadastro:
  ```
{
  "id": 55,
  "categoria": 3,
  "titulo": "DevOps",
  "slug": "novo-livro",
  "descricao": "Livro de Introducao a DevOps",
  "isbn": "978-65-1111-11-1",
  "numeroPaginas": 200,
  "publicacao": "2023-01-01",
  "imagemCapa": "https://raw.githubusercontent.com/viniciosneves/alurabooks/curso-novo/public/imagens/livros/acessibilidade.png",
  "autor": 1,
  "opcoesCompra": [
    {
      "id": 1,
      "titulo": "E-book",
      "preco": 29.9,
      "formatos": [".pdf", ".pub", ".mob"]
    }
  ],
  "sobre": "Compre esse livro e aprenda sobre DevOps."
}
  ```
Após enviar, recebemos 201 Created.

Para verificar a inclusão, podemos realizar um GET:
  ```
https://localhost:8000/livros?categoria=3
  ```
3. Conclusão
GET: envia parâmetros pela URL para buscar dados existentes.

POST: envia dados em JSON para criar novos registros.

Esses métodos são essenciais no HTTP, fundamental em DevOps para manter aplicações web funcionais e otimizadas.
