```markdown
# Teste de API

Este documento descreve os testes de API para as operações de criação, alteração e exclusão de usuários, comentários e posts.
Arquivo da documentação dos testes abaixo:
https://documenter.getpostman.com/view/32464770/2s9YyvBfUW#850be6ca-7aa5-440f-ba4a-a496c88f23d9

## Configuração

Antes de executar os testes, certifique-se de que o ambiente de teste está configurado corretamente. Isso pode incluir a obtenção de tokens de autenticação, configuração de dados iniciais, etc.

## Testes de Usuários

### 1. Criar Usuário

- **Endpoint:** `/api/users`
- **Método:** `POST`
- **Corpo da Solicitação:**
  ```json
  {
    "username": "novousuario",
    "email": "novousuario@example.com",
    "gender": "masculino"
  }
  ```
- **Esperado:** Status de resposta 201 (Created) e retorno do novo usuário criado.
- ![image](https://github.com/HannaHime/Documenta-o-test/assets/151968571/b37a0529-0a7f-4ba9-928b-e873fb732ce5)


### 2. Atualizar Usuário

- **Endpoint:** `/api/users/{id}`
- **Método:** `PUT`
- **Corpo da Solicitação:**
  ```json
  {
    "username": "novonomeusuario"
  }
  ```
- **Esperado:** Status de resposta 200 (OK) e retorno do usuário atualizado.

### 3. Excluir Usuário

- **Endpoint:** `/api/users/{id}`
- **Método:** `DELETE`
- **Esperado:** Status de resposta 204 (No Content).

## Testes de Comentários

### 1. Criar Comentário

- **Endpoint:** `/api/comments`
- **Método:** `POST`
- **Corpo da Solicitação:**
  ```json
  {
    "userId": 1,
    "postId": 1,
    "content": "Este é um novo comentário."
  }
  ```
- **Esperado:** Status de resposta 201 (Created) e retorno do novo comentário criado.

### 2. Atualizar Comentário

- **Endpoint:** `/api/comments/{id}`
- **Método:** `PUT`
- **Corpo da Solicitação:**
  ```json
  {
    "content": "Este é um comentário atualizado."
  }
  ```
- **Esperado:** Status de resposta 200 (OK) e retorno do comentário atualizado.

### 3. Excluir Comentário

- **Endpoint:** `/api/comments/{id}`
- **Método:** `DELETE`
- **Esperado:** Status de resposta 204 (No Content).

## Testes de Posts

### 1. Criar Post

- **Endpoint:** `/api/posts`
- **Método:** `POST`
- **Corpo da Solicitação:**
  ```json
  {
    "userId": 1,
    "title": "Novo Post",
    "body": "Conteúdo do novo post."
  }
  ```
- **Esperado:** Status de resposta 201 (Created) e retorno do novo post criado.

### 2. Atualizar Post

- **Endpoint:** `/api/posts/{id}`
- **Método:** `PUT`
- **Corpo da Solicitação:**
  ```json
  {
    "title": "Post Atualizado",
    "body": "Conteúdo do post atualizado."
  }
  ```
- **Esperado:** Status de resposta 200 (OK) e retorno do post atualizado.

### 3. Excluir Post

- **Endpoint:** `/api/posts/{id}`
- **Método:** `DELETE`
- **Esperado:** Status de resposta 204 (No Content).
```
