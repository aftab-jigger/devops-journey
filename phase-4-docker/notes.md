# Phase 4: Docker & Containerization

## Docker Kya Hai
- Container = halka isolated environment jisme app + saari dependencies bundled hoti hain
- Guarantee deta hai app har machine pe (Mac, server, cloud) same tarah chale
- Solve karta hai "mere machine pe to chal raha tha" wala problem

## Image vs Container
- **Image** = blueprint/recipe (code + dependencies + instructions) — "packed/ready" cheez, static
- **Container** = jab image ko run karte hain, wahi running/active instance banta hai
- `docker run <image>` → agar image local mein nahi hai, Docker Hub se download karta hai, phir container banata hai aur chalata hai

## Dockerfile (Recipe Card)
- Dockerfile = instructions ka set jisse image banti hai (naam exactly "Dockerfile", extension nahi)
- `FROM` → base image (jaise python:3.9-slim)
- `WORKDIR` → container ke andar working folder set karta hai
- `COPY source dest` → files ko container ke andar copy karta hai (dono arguments zaroori hain)
- `CMD ["cmd", "arg"]` → container start hone pe kaunsi command chale
- `docker build -t <name> .` → current folder ke Dockerfile se image banata hai
- `docker run <image-name>` → us image se container chalata hai
- Flow: Dockerfile likho → build karo (image banti hai) → run karo (container chalta hai)

## Container/Image Management
- `docker ps` → sirf running containers, `docker ps -a` → sab (running + stopped)
- `docker images` → sab images list karta hai
- Exit codes: `0` = success, koi bhi non-zero (jaise `1`) = kisi error se band hua
- `docker rm <id>` se container delete, `docker rmi <name>` se image delete
- `docker container prune` se sab stopped containers ek saath clean ho jate hain

## Real Project: GitHub se Todo App Dockerize Karna
- Repo: `nasso/todo-react-express-postgres` (React + Express + Postgres + Prisma + TypeScript, MIT license)
- Backend port 8080, database URL env variable (`DATABASE_URL`) se aati hai
- **Multi-stage build:** Stage 1 ("builder") dependencies install + code compile karta hai; Stage 2 sirf compiled output copy karta hai
- Fayda: chota, saaf final image (dev tools/source code included nahi hote), production ke liye behtar
- Backend Dockerfile pattern: `FROM node AS builder` → build → `FROM node` (fresh) → `COPY --from=builder` → `CMD`

## Nginx for Frontend (Production)
- Dev mode mein Vite proxy karta hai `/api` ko backend tak — production mein ye kaam Nginx karta hai
- `nginx.conf` mein `location /api/` → `proxy_pass http://backend:8080/` (backend = service name)
- Frontend Dockerfile: Stage 1 React build karta hai, Stage 2 (`nginx:alpine`) sirf static files + nginx.conf serve karta hai

## docker-compose.yml (Multi-Service Orchestration)
- Ek hi file mein sab services (db, backend, frontend) define hoti hain
- Har service ke `environment` variables set kar sakte hain (DB credentials, DATABASE_URL)
- Services ek doosre ko **service name** se refer karti hain (jaise `db`, `backend`) — Docker internal DNS resolve kar deta hai
- `depends_on` se start order set hota hai
- `ports: "host:container"` se host ka port container ke port se map hota hai
- `docker compose up --build` se sab services ek saath build+run hoti hain
- `docker compose exec <service> <command>` se chal rahe container ke andar command chala sakte hain (jaise Prisma migrations)
- Poora full-stack app (React + Node + Postgres) ek command se chal jata hai — ye real DevOps ka core skill hai
