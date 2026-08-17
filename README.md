# Task API

A small in-memory CRUD API for managing a to-do list, built with Node.js and Express as part of the FlyRank Backend Track Week 2 assignment. Supports full create, read, update, and delete operations on tasks, with interactive documentation via Swagger UI.

## Install & Run

```bash
npm install
node index.js
```

The server starts on `http://localhost:3000`.

## Endpoints

| Method | Path | Description |
|---|---|---|
| GET | `/` | API info |
| GET | `/health` | Health check |
| GET | `/tasks` | List all tasks |
| GET | `/tasks/:id` | Get one task |
| POST | `/tasks` | Create a task |
| PUT | `/tasks/:id` | Update a task |
| DELETE | `/tasks/:id` | Delete a task |

## Example Request

```
curl -i http://localhost:3000/tasks
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 136
ETag: W/"88-yhLObc+O8DjTIWUoRQ3PTDJaCF4"
Date: Mon, 17 Aug 2026 08:06:55 GMT
Connection: keep-alive
Keep-Alive: timeout=5

[{"id":1,"title":"Buy milk","done":false},{"id":2,"title":"Walk the dog","done":true},{"id":3,"title":"Finish assignment","done":false}]
```

## Swagger UI

Interactive API docs are available at `http://localhost:3000/docs` once the server is running.

 ![Swagger UI screenshot](./swagger-screenshot.png) 

## Notes

- Data is stored in memory only — it resets whenever the server restarts. Persistence is planned for a future stage using a database.