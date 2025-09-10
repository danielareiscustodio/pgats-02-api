# API de Automação Bancária

Esta API permite o registro, login, consulta de usuários e transferências entre usuários, com regras básicas de negócio. O objetivo é servir de base para estudos de testes e automação de APIs.

## Tecnologias
- Node.js
- Express
- Swagger (documentação)

## Instalação

1. Clone o repositório:
   ```bash
   git clone <url-do-repo>
   ```
2. Instale as dependências:
   ```bash
   npm install express swagger-ui-express
   ```

## Como rodar

1. Inicie o servidor:
   ```bash
   node server.js
   ```
2. Acesse a documentação Swagger em: [http://localhost:3000/api-docs](http://localhost:3000/api-docs)

## Endpoints principais

- `POST /users/register` — Registro de usuário
- `POST /users/login` — Login de usuário
- `GET /users` — Listar usuários
- `POST /transfers` — Realizar transferência
- `GET /transfers` — Listar transferências

## Regras de negócio
- Não é permitido registrar usuários duplicados.
- Login exige usuário e senha.
- Transferências acima de R$ 5.000,00 só podem ser feitas para favorecidos.
- O banco de dados é em memória (os dados são perdidos ao reiniciar o servidor).

## Estrutura do projeto
- `controller/` — Rotas e validações HTTP
- `service/` — Lógica de negócio
- `model/` — Dados em memória
- `app.js` — Configuração do app Express
- `server.js` — Inicialização do servidor
- `swagger.json` — Documentação da API

## Testes
Para testar a API, utilize ferramentas como Postman, Insomnia ou scripts automatizados (ex: Supertest).
