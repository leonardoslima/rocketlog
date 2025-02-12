# RocketLog

API de entrega de encomendas.

## Sumário

- [Instalação](#instalação)
- [Configuração](#configuração)
- [Uso](#uso)
- [Rotas](#rotas)
- [Testes](#testes)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Instalação

1. Clone o repositório:
    ```sh
    git clone https://github.com/seu-usuario/rocketlog.git
    cd rocketlog
    ```

2. Instale as dependências:
    ```sh
    npm install
    ```

3. Configure o banco de dados usando Docker:
    ```sh
    docker-compose up -d
    ```

## Configuração

1. Crie um arquivo `.env` baseado no `.env-example`:
    ```sh
    cp .env-example .env
    ```

2. Atualize as variáveis de ambiente no arquivo `.env` conforme necessário.

## Uso

### Desenvolvimento

Para iniciar o servidor em modo de desenvolvimento:
```sh
npm run dev
```

### Produção

Para construir e iniciar o servidor em modo de produção:
```sh
npm run build
npm start
```

## Rotas

### Autenticação
- **POST** `/sessions`: Cria uma nova sessão de usuário (login).

### Usuários
- **POST** `/users`: Cria um novo usuário.

### Entregas
- **POST** `/deliveries`: Cria uma nova entrega.
- **GET** `/deliveries`: Lista todas as entregas.
- **PATCH** `/deliveries/:id/status`: Atualiza o status de uma entrega.

### Logs de Entrega
- **POST** `/delivery-logs`: Cria um novo log de entrega.
- **GET** `/delivery-logs/:delivery_id/show`: Mostra os logs de uma entrega específica.

## Testes

Para rodar os testes:
```sh
npm run test:dev
```

## Tecnologias Utilizadas

- Node.js
- Express
- Prisma
- TypeScript
- Jest
- Docker

## Contribuição

1. Faça um fork do projeto.
2. Crie uma nova branch:
    ```sh
    git checkout -b minha-nova-feature
    ```
3. Faça suas alterações e commit:
    ```sh
    git commit -m 'Adiciona nova feature'
    ```
4. Envie para o repositório remoto:
    ```sh
    git push origin minha-nova-feature
    ```
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a Licença ISC.

