# NirmaanSetu

NirmaanSetu is a workforce skilling and employment outcome platform built with:

- React + Vite frontend
- Java 21 + Spring Boot backend
- one GitHub repository
- one Vercel project
- Vercel Services for frontend/backend composition

## Architecture

```text
GitHub
  │
  └── ONE NirmaanSetu repository
        │
        ├── frontend/  → React + Vite service
        │
        ├── backend/   → Java 21 + Spring Boot container service
        │
        └── vercel.json
                    │
              ONE Vercel project
                    │
          ┌─────────┴─────────┐
          │                   │
        /*                  /api/*
          │                   │
      frontend             backend
```

## Local development

Frontend:

```bash
cd frontend
npm ci
npm run dev
```

Backend:

```bash
cd backend
mvn spring-boot:run
```

The Vite dev server proxies `/api` to the local Spring Boot server.

## Deployment

See `DEPLOY_VERCEL.md`.
