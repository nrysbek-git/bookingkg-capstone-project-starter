# BookingKG — Student Starter

[Русский](README.md) | [English](README_EN.md)

This is the student starter repository for the final DevOps capstone project.
You receive a working application layer and must design, implement, secure, and
document the complete delivery platform.

## Expected application

The final result is a working BookingKG platform. The screenshots show
the expected application; you must build the containers, infrastructure,
Kubernetes deployment, and CI/CD process yourself.

| Sign in | Create account |
| --- | --- |
| ![BookingKG sign in](docs/screenshots/sign-in.png) | ![BookingKG registration](docs/screenshots/register.png) |

### Dashboard

![BookingKG dashboard](docs/screenshots/dashboard.png)

### DevOps assessment

![BookingKG assessment](docs/screenshots/assessment.png)

### Leaderboard

![BookingKG leaderboard](docs/screenshots/leaderboard.png)

### Swagger API documentation

![BookingKG API documentation](docs/screenshots/api-docs.png)

## What you receive

- `frontend/` — React frontend;
- `backend/` — Node.js and Express REST API;
- `database/init.sql` — PostgreSQL schema;
- `ASSIGNMENT.md` — complete technical requirements;
- `PREREQUISITES.md` — required skills, tools, and access;
- `GRADING_RUBRIC.md` — assessment rules;
- `TROUBLESHOOTING.md` — safe diagnostic guidance;
- `COST_AND_CLEANUP.md` — AWS budget and cleanup requirements.

## What you must build

The starter intentionally does not include:

- Dockerfiles or Docker Compose;
- Terraform infrastructure;
- Kubernetes manifests;
- GitHub Actions workflows;
- Helm configuration, because Helm is optional;
- cloud resources, credentials, DNS records, or TLS certificates.

Your implementation must support:

1. a local full-stack deployment at `http://localhost:8080`;
2. an AWS deployment available through a Load Balancer URL;
3. an optional custom domain and HTTPS when a course subdomain is available.

Start with [PREREQUISITES.md](PREREQUISITES.md), then read
[ASSIGNMENT.md](ASSIGNMENT.md) and [GRADING_RUBRIC.md](GRADING_RUBRIC.md).

## Security warning

Never commit real passwords, AWS keys, Terraform state, `.env`, kubeconfig, or
private keys. Students are not required to buy a domain or use a personal bank
card for this project.

