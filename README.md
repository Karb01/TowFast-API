# TowFast-API

TowFast-API é uma aplicação backend desenvolvida para gerenciar serviços de guincho e assistência veicular, oferecendo endpoints RESTful para cadastro, autenticação, gerenciamento de solicitações e integração com sistemas externos.

## Visão Geral

O projeto segue uma arquitetura modular, separando responsabilidades em camadas como controllers, services, repositories e models. Utiliza Node.js com TypeScript, Express para criação das rotas e integração com bancos de dados relacionais (ex: PostgreSQL).

## Funcionalidades

- Cadastro e autenticação de usuários (JWT)
- Gerenciamento de solicitações de guincho
- Listagem e atualização de status de serviços
- Integração com sistemas de pagamento (se aplicável)
- Logs e tratamento de erros centralizado
- Validação de dados de entrada

## Tecnologias Utilizadas

- Node.js
- TypeScript
- Express
- PostgreSQL (ou outro banco relacional)
- Sequelize ou TypeORM (ORM)
- JWT para autenticação
- Dotenv para variáveis de ambiente

## Estrutura de Pastas

```
src/
  controllers/   # Lógica das rotas e requisições
  services/      # Regras de negócio
  repositories/  # Acesso a dados
  models/        # Definição das entidades
  middlewares/   # Middlewares globais (auth, error handler, etc)
  routes/        # Definição das rotas
  config/        # Configurações (DB, env)
  utils/         # Funções utilitárias
```

## Instalação

1. Clone este repositório:
   ```
   git clone https://github.com/seu-usuario/TowFast-API.git
   ```
2. Instale as dependências:
   ```
   npm install
   ```
3. Configure as variáveis de ambiente conforme o arquivo `.env.example`.

## Uso

Inicie o servidor de desenvolvimento:
```
npm run dev
```
Acesse a API em `http://localhost:3000` (ou porta configurada).

## Testes

Execute os testes automatizados (se aplicável):
```
npm test
```

## Contribuição

Contribuições são bem-vindas! Abra uma issue ou envie um pull request.

## Licença

Este projeto está licenciado sob os termos da licença MIT.
