# Phase 4: Docker & Containerization Cheatsheet

| Command / Syntax | Description |
|---|---|
| `docker --version` | Installed Docker version check karta hai |
| `docker run <image>` | Kisi image ko download (agar na ho) karke container run karta hai |
| `docker build -t <name> .` | Current folder ke Dockerfile se image banata hai, naam deta hai (-t = tag) |
| `docker ps` | Sirf currently running containers dikhata hai |
| `docker ps -a` | Saare containers dikhata hai (running + stopped) |
| `docker images` | Saari downloaded/built images list karta hai |
| `docker rm <container-id>` | Kisi stopped container ko delete karta hai |
| `docker rmi <image-name>` | Kisi image ko delete karta hai |
| `docker container prune` | Sab stopped containers ek saath clean karta hai |
| `docker compose up --build` | docker-compose.yml se sab services build+run karta hai |
| `docker compose exec <service> <cmd>` | Chal rahe container ke andar koi command chalata hai |
| `docker compose down` | Sab services ko stop aur remove karta hai |
