# 👋 Hi, I'm Arjun Dwi Bastian

🎓 **Graduated Hacktiv8 (Phase 3)** — Go Backend Developer
💼 **Currently looking for work** — open to full-time, contract, freelance, and collaborations

[![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)](https://go.dev/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![gRPC](https://img.shields.io/badge/gRPC-244c5a?style=for-the-badge&logo=grpc&logoColor=white)](https://grpc.io/)
[![Echo](https://img.shields.io/badge/Echo-FF6B6B?style=for-the-badge&logo=go&logoColor=white)](https://echo.labstack.com/)

📍 Indonesia · 💬 Ask me about Go microservices, REST/gRPC, and Postgres

---

## 🚀 Flagship Project

### 🍱 BagiPangan (formerly ZeroHunger)
> Go microservices platform connecting food donors with recipients. Donors post listings, recipients create requests, claims link them with a 6-digit pickup code.

**Architecture:** `user-service :8081/50051` · `food-service :8082/50052` · `request-service :8083/50053` · `claim-service :8084/50054` · shared `contracts` protobuf repo · `infra` Compose + Postman E2E

**Highlights:**
- JWT auth with donor/recipient roles, bcrypt hashing, refresh flow
- Food listings with quantity reserve/release, nearby search by `request_id` + radius
- Request lifecycle `searching → claimed → completed` with cancel compensation
- Claim lifecycle `waiting_for_pickup → picked_up / cancelled` + Resend email notifications
- Cross-service validation over gRPC (`GetUser`, `GetRequest`, `ReserveFoodQuantity`)
- Docker Compose with HTTP-only host ports, internal gRPC, `DB_SSLMODE` handling

🔗 **github.com/arjundwibastian/BagiPangan**

---

## 🛠️ Tech Stack

| Area | Skills |
|------|--------|
| **Golang Backend** | Go 1.22+, Echo, net/http, REST design, versioned routing `/api/v1`, JWT (access/refresh), auth + role middleware, request validation, custom errors → HTTP/gRPC codes, bcrypt, concurrency, graceful shutdown, testify + mocks, table-driven tests |
| **gRPC / Contracts** | Protobuf, buf, `protoc-gen-go`, unary interceptors (planned), service-to-service clients, `grpc.Dial` + insecure creds for local, timeouts + retries, status mapping |
| **Databases** | PostgreSQL 14+, pgx v5 + pgxpool, GORM, migrations (`001_init.sql`), UUID PKs via `pgcrypto`, FKs + `ON DELETE CASCADE`, UNIQUE constraints, indexes (B-tree/GiST), transactions, compensating actions, connection pooling + `Ping` healthchecks, PostGIS-style nearby queries |
| **DevOps / Tools** | Docker + Compose (multi-service builds with `context: ..`), `.env` + `.env.example` workflow, Git monorepo (converted from 7 repos + submodules), GitHub, Postman collections + environments, Resend API, VS Code launch configs |

---

## 📂 More Projects

| Project | Description | Stack |
|---------|-------------|-------|
| **RentGo** | Car/vehicle rental API — auth, CRUD, bookings | Go, Echo, Postgres |
| **BookLibrary** | Book management service — clean layered structure | Go, Postgres |
| **gaming-house** | Golang CLI + database connection playground | Go, SQL |

---

## 🎓 Experience & Education

**Hacktiv8 — Phase 3 Final Project (2026)**
- Designed and built BagiPangan microservices end-to-end
- Owned proto contracts, Compose orchestration, E2E testing
- Hardened for public release: secret hygiene, port exposure review, README + flow diagram

**Self-directed (2025–2026)**
- Built REST APIs in Go with Postgres + Docker
- Practiced migrations, auth, testing, and deployment

---

## 📊 GitHub Stats

![Arjun's GitHub stats](https://github-readme-stats.vercel.app/api?username=arjundwibastian&show_icons=true&theme=tokyonight&hide_border=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=arjundwibastian&layout=compact&theme=tokyonight&hide_border=true)
![Streak](https://streak-stats.demolab.com?user=arjundwibastian&theme=tokyonight&hide_border=true)

---

## 📫 Contact

- GitHub: https://github.com/arjundwibastian
- LinkedIn: www.linkedin.com/in/arjun-dwi-bastian
- Email: arjundwibastian@gmail.com
- Location: Indonesia — open to remote

⭐ If you like BagiPangan, leave a star — and reach out if you're hiring Go backend.
