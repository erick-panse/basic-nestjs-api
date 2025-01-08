# NestJS API

Este repositório contém uma API construída com NestJS, incluindo suporte a autenticação JWT e integração com Prisma para manipulação de banco de dados. Abaixo estão as instruções para configurar e executar este projeto.

---

## **Requisitos**

Antes de começar, certifique-se de que você tem os seguintes itens instalados:

- **Node.js** (versão recomendada: 18.x ou superior)
- **NPM** (vem com o Node.js)
- **Git** (para clonar o repositório)

---

## **Passos para configuração**

### **1. Clonar o repositório**

Use o comando abaixo para clonar o repositório e acessar a pasta do projeto:

```bash
git clone <URL_DO_REPOSITORIO>
cd <PASTA_DO_REPOSITORIO>
```

---

### **2. Instalar dependências**

Instale todas as dependências necessárias com o seguinte comando:

```bash
npm install
```

---

### **3. Configurar variáveis de ambiente**

Crie um arquivo `.env` na raiz do projeto. Use o arquivo de exemplo (`env.example`) como referência para configurar as variáveis necessárias, como credenciais do banco de dados e JWT Secret.
```bash
DATABASE_URL="postgresql://<Usuario do banco de dados>:<senha>@localhost:<PORT usada pelo BD>/<Nome do BD>?schema=public"
JWT_SECRET='super-secreto'
```
---

### **4. Configurar o banco de dados**

Este projeto utiliza o Prisma para gerenciar o banco de dados. Certifique-se de configurar corretamente as variáveis de ambiente relacionadas ao banco no arquivo `.env`. Após isso, execute os comandos abaixo:

```bash
npx prisma generate   # Gera os clientes do Prisma
npx prisma migrate dev   # Executa as migrações no banco de dados
```

---

### **5. Executar a aplicação**

Você pode rodar a aplicação em diferentes modos, dependendo do ambiente:

- **Modo Desenvolvimento:**
  ```bash
  npm run start:dev
  ```

- **Modo Produção:**
  Antes de rodar em produção, é necessário construir a aplicação:
  ```bash
  npm run build
  npm run start:prod
  ```

---

### **6. Testar a aplicação (opcional)**

Se desejar rodar os testes automatizados:

```bash
npm run test:e2e
```

---

## **Comandos úteis**

### **Scripts do NPM**

| Comando              | Descrição                                        |
|----------------------|--------------------------------------------------|
| `npm run build`      | Constrói o projeto para produção                 |
| `npm run start`      | Inicia a aplicação em produção                   |
| `npm run start:dev`  | Inicia a aplicação em modo de desenvolvimento    |
| `npm run start:prod` | Inicia a aplicação em produção após o build      |
| `npm run test:e2e`   | Roda os testes unitários                         |

---

## **Dependências Principais**

- [NestJS](https://nestjs.com/): Framework para Node.js.
- [Prisma](https://www.prisma.io/): Ferramenta ORM para banco de dados.
- [JWT](https://jwt.io/): Gerenciamento de autenticação.

---
