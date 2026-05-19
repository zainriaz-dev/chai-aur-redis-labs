# Chai Aur Redis - Learning Labs

Hands-on Redis learning labs with Node.js, Express, and ioredis. Includes Docker Compose for local Redis and MongoDB, plus two small apps for practice.

Mentor: Hitesh Choudhary (Chai Aur Code)

## Project structure
- 01 foundation of redis: notes for the foundation video
- 02-setup-local-redis: local Redis and Mongo connection checks
- 03-site-banner: a small banner API backed by Redis
- docker-compose.yml: local Redis and Mongo services

## Prerequisites
- Node.js 18+ (or newer)
- Docker Desktop (for Redis and Mongo)

## Quick start (Docker)
Run Redis and Mongo locally with Docker Compose:

```bash
docker compose up -d
```

## App 1: 02-setup-local-redis
Install and run:

```bash
cd 02-setup-local-redis
npm install
npm run dev
```

Endpoints:
- GET /redis -> Redis ping
- GET /mongo -> Mongo connection check

Environment variables:
- REDIS_URL (default: redis://localhost:6379)
- MONGO_URL (default: mongodb://localhost:27017/chai_aur_mongo)

## App 2: 03-site-banner
Install and run:

```bash
cd 03-site-banner
npm install
npm run dev
```

Endpoints:
- POST /banner -> set banner message (JSON body: { "message": "Hello" })
- GET /banner -> get banner message
- DELETE /banner -> delete banner
- GET /banner/exists -> check if banner exists

Environment variables:
- Redis_URL (default: redis://localhost:6379)

Note: both apps default to port 3000, so run one at a time or change the port in code.
