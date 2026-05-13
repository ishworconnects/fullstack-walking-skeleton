# Fullstack Walking Skeleton

A minimal full-stack application scaffold that connects a SvelteKit frontend, a Deno/Hono API server, PostgreSQL, Flyway database migrations, and Playwright end-to-end testing through Docker Compose.

## Project Overview

This repository is designed as a working baseline for a full-stack web application. It keeps a given system intentionally small while proving that the frontend, backend, database, migrations, and browser tests can run together from the start.

## Architecture

- `client` - SvelteKit frontend served with Vite
- `server` - Deno API service using Hono and PostgreSQL access
- `database` - PostgreSQL service
- `database-migrations` - Flyway migrations for schema setup
- `e2e-tests` - Playwright test project
- `compose.yaml` - Local orchestration for all services

## Tech Stack

- SvelteKit
- Vite
- Deno
- Hono
- PostgreSQL
- Flyway
- Docker Compose
- Playwright

## Project Structure

```text
walking-skeleton/
  client/
  server/
  database-migrations/
  e2e-tests/
  compose.yaml
  project.env
```

## Getting Started

From the application directory:

```bash
cd walking-skeleton
docker compose up --build
```

Default local services:

| Service | URL |
| --- | --- |
| Client | `http://localhost:5173` |
| API server | `http://localhost:8000` |
| PostgreSQL | Docker network service `database` |

## Database Migrations

Flyway runs the SQL migrations in `database-migrations/`. The initial migration creates the base `todos` table used by the application scaffold.

## End-to-End Tests

The `e2e-tests` project is configured with Playwright. It is included in the Compose setup so browser-level tests can be added as the application grows.

## Status

Early full-stack scaffold. The goal is to provide a reliable starting point for future feature work while keeping the application architecture easy to understand.
