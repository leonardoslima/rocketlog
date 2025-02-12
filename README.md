# 🚀 RocketLog

API de entrega 📦 de encomendas.

## 📜 Sumário

- ⚙️ Instalação
- 🔧 Configuração
- ▶️ Uso
- 🌐 Rotas
- 🧪 Testes
- 🛠️ Tecnologias Utilizadas
- 🤝 Contribuição
- 📜 Licença

## ⚙️ Instalação

1. Clone o repositório 🖥️:

   ```sh
   git clone https://github.com/seu-usuario/rocketlog.git
   ```

2. Instale as dependências 📦:

   ```sh
   npm install
   ```

3. Configure o banco de dados usando Docker 🐳:
   ```sh
   docker-compose up -d
   ```

## 🔧 Configuração

1. Crie um arquivo `.env` baseado no `.env-example`:

   ```sh
   cp .env-example .env
   ```

   ```sh
   copy .env-example .env
   ```

2. Atualize as variáveis de ambiente no arquivo `.env` conforme necessário.

## ▶️ Uso

### 🚧 Desenvolvimento

Para iniciar o servidor em modo de desenvolvimento:

```sh
npm run dev
```

### 🚀 Produção

Para construir e iniciar o servidor em modo de produção:

```sh
npm run build
npm start
```

## 🌐 Rotas

### 🔐 Autenticação

- **POST** `/sessions`: Cria uma nova sessão de usuário (🔑 login).
  - Exemplo de body:
  ```json
  {
    "email": "usuario@example.com",
    "password": "senha123"
  }
  ```

### 👤 Usuários

- **POST** `/users`: Cria um novo usuário.
  - Exemplo de body:
  ```json
  {
    "name": "Nome do Usuário",
    "email": "usuario@example.com",
    "password": "senha123"
  }
  ```

### 📦 Entregas

- **POST** `/deliveries`: Cria uma nova entrega.
  - Exemplo de body:
  ```json
  {
    "user_id": "1",
    "description": "Descrição da entrega"
  }
  ```
- **GET** `/deliveries`: 📋 Lista todas as entregas.
- **PATCH** `/deliveries/:id/status`: 🔄 Atualiza o status de uma entrega.
  - Exemplo de body:
  ```json
  {
    "status": "shipped"
  }
  ```

### 📜 Logs de Entrega

- **POST** `/delivery-logs`: 📑 Cria um novo log de entrega.
  - Exemplo de body:
  ```json
  {
    "delivery_id": "1",
    "description": "Descrição do log"
  }
  ```
- **GET** `/delivery-logs/:delivery_id/show`: 🔍 Mostra os logs de uma entrega específica.

## 🧪 Testes

Para rodar os testes 🛠️:

```sh
npm run test:dev
```

## 🛠️ Tecnologias Utilizadas

- 🟢 Node.js
- 🚀 Express
- 🔷 Prisma
- 🟦 TypeScript
- 🧪 Jest
- 🐳 Docker

## 📜 Licença

Este projeto está licenciado sob a Licença ISC. Veja o arquivo LICENSE 📄 para mais detalhes.

