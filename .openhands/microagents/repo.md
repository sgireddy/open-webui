# Repository Summary: open-webui

## 1. Purpose
Open WebUI is an extensible, feature-rich, and user-friendly self-hosted AI platform designed to operate entirely offline. It supports various LLM runners such as Ollama and OpenAI-compatible APIs, and includes a built-in inference engine for Retrieval-Augmented Generation (RAG). The platform is intended as a powerful, privacy-focused AI deployment solution for individuals and organizations.

## 2. General Setup
- **Installation:** The platform can be set up using Docker or Kubernetes (kubectl, kustomize, or helm). It supports both CPU and GPU deployments, and provides multiple Docker Compose files for different configurations.
- **Backend:** Python-based, with dependencies managed via `requirements.txt` and `pyproject.toml`.
- **Frontend:** Svelte-based, with dependencies managed via `package.json`.
- **Development:** Includes scripts for local development (`start.sh`, `dev.sh`), and configuration for both backend and frontend builds.
- **Documentation:** Main documentation is in `README.md` and the `docs/` directory. Additional guides include `INSTALLATION.md`, `CONTRIBUTING.md`, and `TROUBLESHOOTING.md`.

## 3. Repository Structure
- `backend/` — Python backend code and data
- `src/` — Svelte frontend source code (with `lib/` and `routes/` subfolders)
- `docs/` — Documentation and guides
- `cypress/` — End-to-end and integration tests
- `kubernetes/` — Kubernetes deployment manifests
- `docker-compose.*.yaml` — Docker Compose files for various deployment scenarios
- `scripts/` — Utility scripts
- `test/` — Additional tests
- `static/` — Static assets
- `package.json`, `pyproject.toml`, `requirements.txt` — Dependency management
- `Makefile` — Common build and development commands

## 4. CI/CD and GitHub Workflows
The repository uses GitHub Actions for CI/CD, with workflows located in `.github/workflows/`:
- **build-release.yml:** Creates GitHub releases based on changes in `package.json` and `CHANGELOG.md`.
- **deploy-to-hf-spaces.yml:** Deploys the project to HuggingFace Spaces on pushes to `main` or `dev` branches (if the `HF_TOKEN` secret is set).
- **docker-build.yaml:** Builds and publishes Docker images for multiple platforms (amd64, arm64) on pushes to `main`, `dev`, or version tags.
- **format-backend.yaml:** Python backend formatting and build checks for pushes and PRs affecting backend code or dependencies.
- **format-build-frontend.yaml:** Frontend formatting and build checks for pushes and PRs affecting frontend code.
- **release-pypi.yml:** Builds and publishes the Python package to PyPI on pushes to `main` or `pypi-release` branches.
- **integration-test.disabled:** (Disabled) Cypress-based integration tests using Docker Compose.
- **lint-backend.disabled:** (Disabled) Python backend linting using `pylint` and Bun.
- **lint-frontend.disabled:** (Disabled) Frontend linting and type checks using Bun.

Other files in `.github/` include issue templates, pull request templates, and funding configuration.
