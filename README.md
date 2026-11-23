# Task API (SYD204)

A Task List REST API built three ways: in-memory, MySQL (single file), and MVC.

## Setup
```bash
npm install
cp .env.example .env     # then fill in YOUR Aiven username and password
```
Run `database/schema.sql` once in MySQL Workbench, then check the connection:
```bash
node test-db.js
```

## Run
```bash
npm start          # Part 2: single-file MySQL API (server.js)
npm run start:mvc  # Part 3: MVC API (server-mvc.js)
```

## Endpoints
| Method | URL          | Description            |
|--------|--------------|------------------------|
| GET    | /            | Health check           |
| GET    | /tasks       | List all tasks         |
| GET    | /tasks/:id   | Get one task           |
| POST   | /tasks       | Create a task          |
| PUT    | /tasks/:id   | Replace title + completed |
| PATCH  | /tasks/:id   | Partial update         |
| DELETE | /tasks/:id   | Delete a task          |

## Structure
```
server-mvc.js → src/routes → src/controllers → src/models → src/db.js → MySQL
```
> Never commit `.env`. It is listed in `.gitignore`.
