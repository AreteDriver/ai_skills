---
name: Docker
category: devops
priority: 5
description: Best practices for Dockerfiles and container workflows.
---

# Docker Skill

## Dockerfile Best Practices
- Use specific base image tags, not `latest`.
- Multi-stage builds to minimize final image size.
- Order layers from least to most frequently changed (dependencies before source).
- Combine RUN commands to reduce layers: `RUN apt-get update && apt-get install -y ...`.
- Use `.dockerignore` to exclude `.git`, `node_modules`, build artifacts.
- Run as non-root user: `USER appuser`.
- Set `HEALTHCHECK` for production images.

## Compose
- Pin image versions in `docker-compose.yaml`.
- Use named volumes for persistent data.
- Define resource limits (`mem_limit`, `cpus`).
- Use `depends_on` with health checks, not just service ordering.

## Security
- Scan images: `docker scout`, `trivy`, or `grype`.
- Don't store secrets in image layers — use runtime env vars or secret mounts.
- Minimize installed packages to reduce attack surface.
