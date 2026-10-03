# Projeto Todo

Lista de tarefas simples, feita para praticar o desenvolvimento de uma aplicação completa: banco de dados, API e frontend se comunicando entre si.

## Funcionalidades

- Cadastrar tarefas
- Listar as tarefas cadastradas
- Editar o texto de uma tarefa
- Marcar uma tarefa como realizada (ou desmarcar)
- Excluir tarefas

## Tecnologias

- **Banco de dados:** MySQL
- **Backend:** Node.js, Express, mysql2, cors e dotenv
- **Frontend:** HTML, CSS, JavaScript e Axios

## Estrutura

```
projeto_todo
├── backend
│   ├── db.sql
│   ├── package.json
│   └── src
│       ├── server.js
│       ├── config/db.js
│       ├── models/taskModel.js
│       ├── controllers/taskController.js
│       └── routes/taskRoutes.js
└── frontend
    ├── index.html
    ├── style.css
    └── script.js
```

## Banco de dados

Banco `todo_db`, com a tabela `tasks`:

| Campo     | Descrição                                      |
|-----------|------------------------------------------------|
| id        | Identificação automática da tarefa             |
| tarefa    | Texto da tarefa                                |
| realizada | Indica se a tarefa foi concluída (padrão: não) |

## Endpoints da API

| Método | Rota           | Descrição                         |
|--------|----------------|-----------------------------------|
| POST   | /api/tasks     | Cria uma tarefa                   |
| GET    | /api/tasks     | Lista as tarefas                  |
| PUT    | /api/tasks/:id | Altera uma tarefa (texto/status)  |
| DELETE | /api/tasks/:id | Exclui uma tarefa                 |

## Como executar

1. Execute o arquivo `backend/db.sql` no MySQL (pelo DBeaver, por exemplo) para criar o banco `todo_db` e a tabela `tasks`.
2. Na pasta `backend`, instale as dependências e inicie a API:
```bash
   npm install
   npm run dev
```
3. Abra o arquivo `frontend/index.html` no navegador.

A API roda em `http://localhost:3000`. Se o seu MySQL usar outro usuário ou senha, crie um arquivo `.env` na pasta `backend` com `DB_HOST`, `DB_USER`, `DB_PASSWORD` e `DB_NAME`.

## Autor

Giovany Wittlich
