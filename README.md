# docker-cadvisor

Cadvisor docker

## Build

```bash
docker buildx prune
docker buildx build --platform linux/amd64,linux/arm64 -t tinpotnick/cadvisor:1.0.0 . --push
```

## Current Version of Prometheus

Latest versions on [GitHub](https://github.com/google/cadvisor/releases)

```bash
Cadvisor v0.55.1
```
