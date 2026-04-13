# Fullstack Walking Skeleton

Coursework for the Aalto Web Software Development course.

## Project

The main project lives in `walking-skeleton/` and contains:

- a Svelte client
- a Deno server
- PostgreSQL with Flyway migrations
- Playwright end-to-end tests

## Structure

```text
walking-skeleton/
  client/
  server/
  database-migrations/
  e2e-tests/
  compose.yaml
  project.env
```

## Run the Application

From the repository root:

```powershell
cd walking-skeleton
docker compose up --build
```

Services:

- client: `http://localhost:5173`
- server: `http://localhost:8000`

## Run the Playwright Test

Start the application first, then run:

```powershell
cd walking-skeleton
docker compose run --rm --entrypoint=npx e2e-tests playwright test
```

## Notes

- The client uses SvelteKit routing with pages and a shared layout.
- The server exposes `/api/todos`.
- Database schema is managed through Flyway migrations.
