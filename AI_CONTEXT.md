# AI Context for GitHub Actions Demo

## Project Overview
- **Purpose**: Demonstrating CI/CD pipelines using GitHub Actions for a containerized application.
- **Tech Stack**: GitHub Actions, Docker, Node.js (backend/frontend assumed), MySQL.
- **Architecture**: Microservices-style setup with separate backend, frontend, and database services, managed by Docker Compose.

## Current State
- **Version**: 0.1.0
- **Status**: In Development
- **Last Updated**: 2026-05-03

## File Structure
```
.github/workflows/
  - ci.yml (Continuous Integration)
  - cd.yml (Continuous Deployment)
backend/
frontend/
mysql/
nginx/
docker-compose.yml
```

## Key Components
### CI Workflow
- **Location**: `.github/workflows/ci.yml`
- **Purpose**: Builds and pushes Docker images to Docker Hub.

### CD Workflow
- **Location**: `.github/workflows/cd.yml`
- **Purpose**: Deploys the application using SSH to a remote server.

## Known Issues
- `cd.yml` has syntax errors (`runs_on` instead of `runs-on`).
- `cd.yml` SSH action configuration is incomplete.

## Development Notes
- The project uses GitHub Secrets for Docker Hub credentials and likely will need them for SSH deployment.
