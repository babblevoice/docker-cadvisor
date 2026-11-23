# docker-cadvisor

![Nightly tests](https://github.com/babblevoice/docker-cadvisor/actions/workflows/nightly.yml/badge.svg)

Cadvisor docker

## Build

A release tag is the only thing that publishes an image. `.github/workflows/release.yml` builds it for amd64 and arm64, each on its own native runner, starts it and asks it for `/metrics`, then pushes `tinpotnick/cadvisor:X.Y.Z` and nothing else: no `latest`, `1.0`, `1`, `main` or `sha-…`. [AGENTS.md](AGENTS.md) has the rules: who may tag what, the run before a pull request, and hotfixes.

```bash
git tag v1.1.0-rc.1 && git push origin v1.1.0-rc.1   # a pre-release, to try out
git tag v1.1.0 && git push origin v1.1.0             # a full release
```

To build one to try, for the platform you are on, into your local Docker and pushing nothing:

```bash
docker build -t docker-cadvisor:test .
```

## Current Version of cAdvisor

Latest versions on [GitHub](https://github.com/google/cadvisor/releases)

```bash
Cadvisor v0.56.2
```
