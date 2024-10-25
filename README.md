# Spring-Data-JPA

Este projeto é uma API RESTful desenvolvida em Spring Boot com foco no uso do Spring Data JPA para gerenciar livros, autores, editoras e suas avaliações.

## Tecnologias

- **Spring Boot**
- **Spring Data JPA**
- **Hibernate**
- **PostgreSQL** (ou outro banco de dados de sua escolha)

## Entidades Principais

- **BookModel**: Representa um livro e conecta autores, editoras e resenhas.
- **AuthorModel**: Captura informações sobre autores.
- **PublisherModel**: Gerencia editoras.
- **ReviewModel**: Representa resenhas de livros.

## Endpoints da API

### GET /bookstore/books

Retorna uma lista de todos os livros.

**Exemplo de Requisição:**

```http
GET /bookstore/books
```
Exemplo de Resposta:

```json
[
  {
    "id": "uuid-do-livro",
    "title": "O Senhor dos Anéis",
    "publisher": "Penguin Random",
    "authors": ["J.R.R. Tolkien"],
    "review": "Um clássico da literatura fantástica!"
  }
]
```

### POST /bookstore/books
Adiciona um novo livro.

Exemplo de Requisição:

```http
POST /bookstore/books
Content-Type: application/json
```

Corpo da Requisição:

```json
{
  "title": "Penguin Random",
  "publisherId": "c49fb56e-b8dd-4d19-934a-28fc1681ddf0",
  "authorIds": ["9d6dfd27-7ff1-4e26-aa99-1bdc40c50ff0"],
  "reviewComment": "Random House is an imprint and publishing group of Penguin Random House..."
}
```

Exemplo de Resposta:

```json
{
  "id": "uuid-do-livro",
  "title": "Penguin Random",
  "publisher": "Penguin Random",
  "authors": ["Author Name"],
  "review": "Random House is an imprint and publishing group of Penguin Random House..."
}
```

### DELETE /bookstore/books/{id}

Deleta um livro pelo ID.

Exemplo de Requisição:

```http
DELETE /bookstore/books/{id}
```
```json
{
  "message": "Book deletado com sucesso"
}

```























