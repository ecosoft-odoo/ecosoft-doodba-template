[![Doodba deployment](https://img.shields.io/badge/deployment-doodba-informational)](https://github.com/Tecnativa/doodba)
[![Last template update](https://img.shields.io/badge/last%20template%20update-v8.4.1-informational)](https://github.com/Tecnativa/doodba-copier-template/tree/v8.4.1)
[![Odoo](https://img.shields.io/badge/odoo-v18.0-a3478a)](https://github.com/odoo/odoo/tree/18.0)
[![BSL-1.0 license](https://img.shields.io/badge/license-BSL--1.0-success})](LICENSE)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://pre-commit.com/)

# Ecosoft Doodba Template (Odoo 18.0)

## About

This repository provides a **ready-to-use template** for deploying **Odoo 18.0** using
[Doodba](https://github.com/Tecnativa/doodba). It is designed to help teams quickly set
up a **standardized Odoo project** with:

- Pre-configured development and production environments.
- CI/CD integration via GitHub Actions.
- Docker-based deployment using `docker compose`.

**Key Benefits:**

- **Consistency** — same structure for every project.
- **Speed** — start development within minutes.
- **Automation** — build, test, and deploy via GitHub Actions.
- **Flexibility** — supports staging and production environments.

## Quick Start

1. **Fork this repository**

   - Click the `Fork` button on GitHub to create your own copy.

2. **Clone your fork**

   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```

3. **Set up environment variables**

   ```bash
   cp .docker/db-access.env.example .docker/db-access.env
   cp .docker/db-creation.env.example .docker/db-creation.env
   cp .docker/odoo.env.example .docker/odoo.env
   ```

   Edit the `.env` files to set up your environment variables.

4. **Build and run the containers**
   ```bash
   docker compose -f prod.yaml build
   docker compose -f prod.yaml up -d
   ```

## CI/CD Workflow

This template includes **GitHub Actions** for automated build & deployment:

- `18.0` branch: Deploy to **Production** - Trigger: Push to `18.0` - Actions: - Build
  Docker image using prod.yaml - Push image to GitHub Container Registry (GHCR)
  <!-- - Deploy to production -->
  <!-- - `develop` branch: Deploy to **Staging**
      - Trigger: Push to develop
      - Actions:
          - Build Docker image using prod.yaml
          - Push image to GitHub Container Registry (GHCR)
          - Deploy to staging -->

**NOTE**: if you want to use github action, you need to add the following secrets to
your repository:

- TOKEN_GITHUB

# Credits

This project is maintained by: Ecosoft
