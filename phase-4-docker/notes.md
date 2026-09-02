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
