## Fullstack Microservices Course with NX Monorepo, Fastify, NestJS, tRPC, Docker, Kafka, Redis, PostgreSQL, and Prisma

## 🧠 Overview
This course will walk you through building a modern microservices-based architecture using a monorepo setup with [Nx](https://nx.dev). It includes services using **Fastify**, **NestJS**, **tRPC**, and integrates **Kafka**, **Redis**, **PostgreSQL**, and **Prisma ORM**.

### 🔧 Tools & Technologies
- **Nx** - Monorepo management
- **Fastify** - Lightweight web server
- **NestJS** - Scalable server-side app framework
- **tRPC** - Type-safe API communication
- **Docker** - Containerized development
- **Kafka** - Messaging/Event Streaming
- **Redis** - Cache & pub/sub
- **PostgreSQL** - Database
- **Prisma** - ORM for PostgreSQL

---

## 📁 Folder Structure
```
microservices-course/
├── apps/
│   ├── gateway/               # API Gateway (Fastify + tRPC)
│   ├── auth-service/          # Authentication (NestJS)
│   ├── user-service/          # User profile service (NestJS)
│   └── notification-service/  # Redis + Kafka for notifications
│
├── libs/
│   ├── shared/                # Shared types and utilities
│   ├── database/              # Prisma schema & helpers
│   └── kafka-client/          # Kafka client setup
│
├── docker/
│   └── dev/                   # Docker Compose setup for local dev
│
├── .env                      # Global env variables
├── docker-compose.yml        # Full infra config
├── nx.json
├── package.json
└── README.md
```

---

## 📚 Course Files (40 Total)
Each file will be accompanied with full explanation and comments.

#### 01. `nx workspace init`
> Initialize a monorepo with `npx create-nx-workspace@latest`

#### 02. `apps/gateway/main.ts`
> Fastify server with tRPC router

#### 03. `apps/gateway/router.ts`
> Register routes, schemas

#### 04. `libs/shared/types.ts`
> Shared types between services (Zod)

#### 05. `apps/auth-service/main.ts`
> NestJS entry point with Auth module

#### 06. `apps/auth-service/auth.module.ts`
> NestJS module setup

#### 07. `apps/auth-service/auth.controller.ts`
> Login/Register endpoints

#### 08. `apps/auth-service/auth.service.ts`
> Auth logic + JWT handling

#### 09. `libs/database/prisma.ts`
> Initialize Prisma client

#### 10. `libs/database/schema.prisma`
> Prisma schema for users, tokens

#### 11. `apps/user-service/user.module.ts`
> User service module

#### 12. `apps/user-service/user.controller.ts`
> User routes

#### 13. `apps/user-service/user.service.ts`
> Business logic

#### 14. `apps/notification-service/main.ts`
> Kafka + Redis consumer app

#### 15. `libs/kafka-client/index.ts`
> Kafka producer/consumer setup

#### 16. `apps/auth-service/kafka.events.ts`
> Send user-created event

#### 17. `apps/notification-service/redis.client.ts`
> Redis publisher/subscriber

#### 18. `apps/notification-service/email.sender.ts`
> Trigger notifications

#### 19. `libs/database/migrate.ts`
> DB migration runner

#### 20. `docker/dev/Dockerfile.gateway`
> Fastify gateway Dockerfile

#### 21. `docker/dev/Dockerfile.auth`
> Auth Dockerfile

#### 22. `docker/dev/Dockerfile.user`
> User Dockerfile

#### 23. `docker/dev/Dockerfile.notification`
> Notification Dockerfile

#### 24. `docker-compose.yml`
> Infra with Redis, Postgres, Kafka, Zookeeper

#### 25. `libs/shared/env.ts`
> Global env helper (dotenv-safe)

#### 26. `apps/auth-service/guards/jwt.guard.ts`
> Protect routes with JWT

#### 27. `apps/user-service/user.kafka.ts`
> Listen to user update events

#### 28. `apps/user-service/user.dto.ts`
> DTOs for user input/output

#### 29. `apps/gateway/auth.client.ts`
> Connect to Auth from gateway

#### 30. `apps/gateway/user.client.ts`
> Connect to User from gateway

#### 31. `apps/gateway/health.ts`
> Healthcheck endpoint

#### 32. `apps/gateway/middleware/logger.ts`
> Request logger

#### 33. `apps/gateway/trpc.router.ts`
> tRPC router setup

#### 34. `libs/shared/errors.ts`
> Unified error handling

#### 35. `libs/shared/logger.ts`
> Winston logger wrapper

#### 36. `libs/shared/validation.ts`
> Zod validators

#### 37. `apps/auth-service/tests/auth.e2e-spec.ts`
> E2E test for login/signup

#### 38. `apps/user-service/tests/user.e2e-spec.ts`
> E2E test for user service

#### 39. `apps/gateway/tests/gateway.e2e-spec.ts`
> E2E for gateway integration

#### 40. `README.md`
> Full course instructions, setup guide, usage

