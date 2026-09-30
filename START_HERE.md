# NirmaanSetu — Vercel Services Ready

This build is prepared for **one GitHub repository + one Vercel project using Vercel Services**.

## Architecture

```text
NirmaanSetu/
├── vercel.json                 # Services configuration
├── frontend/                   # React + Vite service
└── backend/                    # Java 21 + Spring Boot container service
    └── Dockerfile.vercel
```

Vercel routes traffic on one shared domain:

```text
/api/*  → backend service
/*      → frontend service
```

The backend service is a container because Spring Boot is not being deployed as a Vercel-native frontend framework.

Do not create separate GitHub repositories or separate Vercel projects.
