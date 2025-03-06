## Aplicativo de Gerenciamento de Metas

Este é um aplicativo desenvolvido para o gerenciamento eficiente de metas, permitindo o cadastro de objetivos, definição de frequência semanal e monitoramento do progresso. A aplicação organiza as metas concluídas por dia, horário e semana, proporcionando uma experiência fluida e escalável.

## Características do Projeto:

✔ Cadastro de Metas – Permite a definição de objetivos e a frequência com que devem ser realizados.
<br>
✔ Acompanhamento de Progresso – Barra de progresso que evolui até 100% conforme as metas são concluídas.
<br>
✔ Organização de Metas Concluídas – Visualização das metas finalizadas por dia, horário e semana.
<br>
✔ Desenvolvimento Moderno – Utilização de React, Tailwind, TypeScript e outras tecnologias modernas.
<br>
✔ Interface Intuitiva – Design pensado para facilitar o uso e garantir a fluidez da navegação.
<br>
✔ Performance Otimizada – Código leve e rápido, com foco na eficiência de carregamento.

## Tecnologias Utilizadas

### Backend

- **Node.js** – Ambiente de execução JavaScript para construir o servidor.
- **Fastify** – Framework web rápido e eficiente para criação de APIs.
- **Drizzle ORM** – ORM moderno para interação com o banco de dados.
- **PostgreSQL** – Banco de dados relacional para armazenamento de dados.
- **Zod** – Biblioteca para validação de esquemas de dados.
- **Day.js** – Biblioteca para manipulação de datas.
- **CUID2** – Geração de IDs únicos e seguros.
- **TypeScript** – Adiciona tipagem estática ao JavaScript para maior segurança e produtividade.
- **TSX** – Ferramenta para executar TypeScript diretamente sem compilação prévia.
- **Fastify CORS** – Middleware para habilitar CORS (Cross-Origin Resource Sharing).
- **Fastify Type Provider Zod** – Integração do Zod com o Fastify para validação de tipos.

### Ferramentas de Desenvolvimento

- **Biome** – Ferramenta para linting e formatação de código.
- **Drizzle Kit** – CLI para gerenciamento de migrações e schemas do Drizzle ORM.
- **TypeScript** – Adiciona tipagem estática ao JavaScript.
- **Postgres** – Driver para conexão com o banco de dados PostgreSQL.

## Como Rodar o Projeto Localmente

### Pré-requisitos

- Node.js (versão 18 ou superior)
- npm ou yarn (gerenciadores de pacotes)
- Docker

### Passos

1. Clone o repositório:
   ```bash
   git clone https://github.com/JPerrut/MetasBack.git
   ```
2. Acesse a pasta do projeto:
   ```bash
   cd seu-repositorio
   ```
3. Inclua o documento .env na aplicação
   ```bash
   DATABASE_URL="postgresql://usuario:senha@localhost:5432/inorbit"
   ```
4. Inclua o documento docker-compose.yml

   ```bash
   name: pocket-js-server

   services:
   pg:
       image: bitnami/postgresql:13.16.0
       ports:
       - '5432:5432'
       environment:
       - POSTGRES_USER=usuario
       - POSTGRES_PASSWORD=senha
       - POSTGRES_DB=inorbit
   ```

5. Instale as dependências:
   ```bash
   npm install
   ```
6. Inicialize o container docker

   ```bash
   docker compose up -d
   ```

7. Inicie o servidor de desenvolvimento:

   ```bash
   npm run dev
   ```

8. Crie e migre o banco de dados

   ```bash
   npx drizzle-kit generate
   npx drizzle-kit migrate
   ```

9. Visualize o banco de dados
   ```bash
   npx drizzle-kit studio
   ```

## Rotas para Teste

Abaixo estão os caminhos disponíveis para testar as rotas da aplicação localmente:

### Metas

- **Listar todas as metas**:

  ```bash
  GET http://localhost:3333/goals
  ```

- **Listar metas pendentes**:
  ```bash
  GET http://localhost:3333/pending-goals
  ```

### Completions

- **Listar todas as completions**:
  ```bash
  GET http://localhost:3333/completions
  ```
- **Criar uma nova completion**:
  ```bash
  POST http://localhost:3333/completions
  ```

### Como Testar

Você pode testar as rotas usando ferramentas como [Postman](https://www.postman.com/), [Insomnia](https://insomnia.rest/) ou diretamente no terminal com `curl`.

#### Exemplo com `curl`:

```bash
curl -X GET http://localhost:3333/goals
```

## Contribuição

### Contribuições são bem-vindas! Siga os passos abaixo:

1. Faça um fork do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`).
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`).
4. Faça push para a branch (`git push origin feature/nova-feature`).
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a <a href="https://opensource.org/license/mit">MIT License</a>.

## Contato

### Se tiver dúvidas ou sugestões, entre em contato:

Nome: João Perrut <br>
Email: joaoperrutc@gmail.com <br>
Linkedin: https://www.linkedin.com/in/perrut/
