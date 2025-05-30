# 🚀 DevHiveNestJs

**DevHiveNestJs** is a full-stack developer platform to manage internal resources, secrets, file uploads, and background jobs—powered by modern backend and frontend stacks.

> A clean and modular production-ready starter using:
> NestJS + Fastify • PostgreSQL + Prisma • Keycloak • Redis + BullMQ • MinIO • Angular • Sentry

---

## 📦 Stack Overview

| Layer      | Technology             |
|------------|------------------------|
| Backend    | NestJS + Fastify       |
| Database   | PostgreSQL + Prisma    |
| Auth       | Keycloak               |
| File Store | MinIO (S3-compatible)  |
| Queue      | BullMQ + Redis         |
| Cache      | Redis                  |
| Frontend   | Angular                |
| Monitoring | Sentry                 |

---

## 📁 Monorepo Structure

```bash
devhive/
│
├── backend/
│   ├── src/
│   │   ├── auth/ (Keycloak strategy, guards)
│   │   ├── projects/
│   │   ├── resources/
│   │   ├── files/
│   │   ├── jobs/
│   │   ├── common/
│   │   └── main.ts
│   ├── prisma/
│   └── docker/
│
├── frontend/
│   └── angular-app/
│       ├── src/app/
│       └── ...
│
├── docs/
│   ├── README.md
│   ├── setup-keycloak.md
│   ├── setup-minio.md
│   └── architecture.png
│
├── docker-compose.yml
└── .env.example
````

---

## 🗺️ Roadmap

### 🔹 Phase 1 – Core API and Auth

* [x] Setup NestJS with Fastify
* [x] Setup PostgreSQL + Prisma
* [x] Integrate Keycloak (AuthN + AuthZ)
* [ ] CRUD for Projects
* [ ] CRUD for Secrets / Resources
* [ ] Basic Audit Logs

### 🔹 Phase 2 – File Storage, Caching & Queuing

* [ ] Integrate MinIO for S3 file uploads
* [ ] Setup Redis for caching project metadata
* [ ] Setup BullMQ for async job handling
* [ ] Add background job: Notify expiring secrets

### 🔹 Phase 3 – Frontend & Monitoring

* [ ] Build Angular Admin UI
* [ ] Connect UI to backend with Auth flow
* [ ] Integrate Sentry for FE + BE monitoring
* [ ] Add analytics/events tracking (optional)

---

## 🧑‍💻 Developer Setup

```bash
git clone https://github.com/JawherKl/dev-hive-nestjs
cd devhive
cp .env.example .env
docker-compose up -d
```

```bash
cd backend
pnpm install
pnpm start:dev
```

```bash
cd frontend
pnpm install
pnpm start
```

---

## 🧪 Testing

* Coming soon (e2e and unit tests with `Jest` and `Supertest`)

---

## 🧠 Inspirations

* [NestJS Docs](https://docs.nestjs.com/)
* [Prisma](https://www.prisma.io/)
* [Keycloak](https://www.keycloak.org/)
* [MinIO](https://min.io/)
* [BullMQ](https://docs.bullmq.io/)
* [Sentry](https://sentry.io/)

---

## 📜 License

MIT – Made by [JawherKl](https://github.com/JawherKl)

