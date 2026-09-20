# Movie Collection API

Simple Movie Collection REST API built with Node.js + Express, using an in-memory array for storage (no database — data resets when the server restarts).

## Setup

```bash
npm install
npm start
```

Server runs at `http://localhost:3000`. Open that URL in a browser to use the frontend (`index.html`), which is served automatically.

## Endpoints

| Method | Route              | Description                          |
|--------|---------------------|---------------------------------------|
| GET    | `/api/movies`        | Get all movies                        |
| GET    | `/api/movies/:id`    | Get a single movie by id              |
| POST   | `/api/movies`        | Add a new movie                       |

### POST /api/movies body

```json
{
  "title": "Inception",
  "genre": "Science Fiction",
  "year": 2010
}
```

`id` is assigned automatically. `title`, `genre`, and `year` are required — missing any of them returns a `400` error.
