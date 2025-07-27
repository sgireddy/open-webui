# open-webui Repository Summary

## Purpose
Open WebUI is an extensible, feature-rich, and user-friendly self-hosted AI platform designed to operate entirely offline. It supports various LLM runners (Ollama, OpenAI-compatible APIs), provides a built-in inference engine for RAG, and offers a powerful, customizable AI deployment solution for individuals and enterprises.

## General Setup
- Backend (Python, FastAPI) and frontend (Svelte, TypeScript) are included.
- Can be run with Docker, Docker Compose, or Kubernetes (manifests in `kubernetes/`).
- Backend dependencies managed via `pyproject.toml` and `requirements.txt`.
- Frontend dependencies managed via `package.json` and built with Node.js tooling.
- Includes scripts for development, deployment, and model management.

## Repository Structure
- `backend/`: Python FastAPI backend, including core logic, models, routers, and tasks
- `src/`: Svelte/TypeScript frontend source code
- `kubernetes/`: Kubernetes manifests for deployment
- `docs/`: Documentation, contributing, and security guidelines
- `.github/`: GitHub Actions workflows, issue templates, and PR templates
- `docker-compose.yaml` and variants: Compose files for different deployment scenarios
- `Makefile`, `run.sh`, `run-compose.sh`: Helper scripts for building and running the app

## CI Checks / Workflows
- `.github/workflows/build-release.yml`: Release workflow for main branch
- `.github/workflows/docker-build.yaml`: Builds and publishes Docker images on push to main/dev/tags
- `.github/workflows/format-backend.yaml`: Python backend CI (main/dev branches, backend/ and pyproject.toml)
- `.github/workflows/format-build-frontend.yaml`: Frontend build CI (main/dev branches, ignores backend)
- `.github/workflows/release-pypi.yml`: Publishes Python package to PyPI on push to main/pypi-release
- `.github/workflows/deploy-to-hf-spaces.yml`: Deploys to HuggingFace Spaces on push to main/dev
- Some workflows (lint, integration-test) are present but disabled

---
For more details, see the main README and docs/README.md.