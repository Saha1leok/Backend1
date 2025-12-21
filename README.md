# 🚀 Node.js + Express — Lightweight CRUD API

Short project description
This repository contains a minimal RESTful API built with Node.js and Express that demonstrates basic CRUD (Create, Read, Update, Delete) operations. Data is persisted in a local `data.json` file (NoSQL-style, file-based storage) so you don't need a separate database.

---

## Prerequisites
- Node.js (v12+ recommended)
- npm (comes with Node.js)

---

## How to install dependencies

1. Clone the repository (if you haven't already):
```bash
git clone https://github.com/Saha1leok/Backend1.git
cd Backend1
```

2. Install dependencies:
```bash
npm install
```

---

## How to run the server

Start the server with:
```bash
node server.js
```

By default the server listens on port 3000. After starting you should see:
```
Server started on port 3000
```

(If your project includes an `npm start` script, you can also run `npm start`.)

---

## Project structure (example)
- `server.js` — main Express server file
- `data.json` — local file that stores objects persisted by the API
- `package.json` — project metadata and scripts

---

## List of API routes

Diagnostic routes
- GET /  
  Health check — returns a simple alive response.

- GET /hello  
  Returns a friendly greeting.

- GET /time  
  Returns current server timestamp.

- GET /status  
  Returns basic operational status.

CRUD routes
- GET /objects  
  Retrieve all stored objects.

- POST /objects  
  Create and store a new object. The server assigns a unique `id`.

- PUT /objects/:id  
  Update an existing object by its `id`.

- DELETE /objects/:id  
  Remove an object by its `id`.

Notes:
- All request and response bodies are JSON.
- IDs are typically numeric or string depending on implementation in `server.js`.

---

## Example Postman requests

1) Fetch all objects
- Method: GET  
- URL: `http://localhost:3000/objects`

2) Create a new object
- Method: POST  
- URL: `http://localhost:3000/objects`  
- Headers:
  - `Content-Type: application/json`
- Body (raw JSON):
```json
{
  "name": "Buy milk"
}
```

Example curl:
```bash
curl -X POST http://localhost:3000/objects \
  -H "Content-Type: application/json" \
  -d '{"name":"Buy milk"}'
```

3) Update an object
- Method: PUT  
- URL: `http://localhost:3000/objects/{id}` (replace `{id}` with the actual id)  
- Headers:
  - `Content-Type: application/json`
- Body (raw JSON):
```json
{
  "name": "Buy bread"
}
```

Example curl:
```bash
curl -X PUT http://localhost:3000/objects/1 \
  -H "Content-Type: application/json" \
  -d '{"name":"Buy bread"}'
```

4) Delete an object
- Method: DELETE  
- URL: `http://localhost:3000/objects/{id}`

Example curl:
```bash
curl -X DELETE http://localhost:3000/objects/1
```

---

## Technical notes
- All modifications are saved to `data.json` (file-based persistence).
- This project is intended for learning and simple demos — consider adding validation, error handling, and a real database for production use.

---

If you want, I can:
- Commit this README.md to your repository,
- Add an example `server.js` with comments and route implementations,
- Add an `npm start` script to `package.json`.
