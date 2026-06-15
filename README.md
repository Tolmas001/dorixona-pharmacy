# Dorixona Project

Loyiha ikki papkaga ajratilgan:

- `backend` - Fastify, Prisma, PostgreSQL API
- `frontend` - React, Vite frontend

## Backend

Docker Desktop ishga tushgan bo'lishi kerak.

```bash
cd backend
docker compose up -d
pnpm exec prisma generate
pnpm run prisma:deploy
pnpm run dev
```

Backend default port:

```text
http://127.0.0.1:3000
```

Health check:

```text
http://127.0.0.1:3000/health
```

Auth endpointlar:

- `POST /auth/register`
- `POST /auth/verify-otp`
- `POST /auth/resend-otp`
- `POST /auth/login`

## Frontend

```bash
cd frontend
npm install
npm run dev
```

Frontend:

```text
http://127.0.0.1:5173/api/register
http://127.0.0.1:5173/api/login
```

Frontend backendga Vite proxy orqali ulanadi:

```text
/server -> http://127.0.0.1:3000
```
