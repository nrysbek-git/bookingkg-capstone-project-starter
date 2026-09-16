# BookingKG — Student Project

**Language:** [Русский](README.md) · English

This repository is the student project for the final BookingKG DevOps capstone.

Students receive a ready application layer:

- `frontend/` — BookingKG React interface;
- `backend/` — Node.js/Express REST API;
- `database/init.sql` — PostgreSQL schema and sample destinations.

Students independently implement Docker packaging, Docker Compose, Terraform,
AWS infrastructure, Kubernetes manifests, EKS delivery, and CI/CD.

## Documentation

- [ASSIGNMENT_EN.md](ASSIGNMENT_EN.md) — assignment and acceptance criteria;
- [PREREQUISITES_EN.md](PREREQUISITES_EN.md) — knowledge, tools, and access;
- [GRADING_RUBRIC_EN.md](GRADING_RUBRIC_EN.md) — grading and defense rules;
- [TROUBLESHOOTING_EN.md](TROUBLESHOOTING_EN.md) — diagnostic guidance;
- [COST_AND_CLEANUP_EN.md](COST_AND_CLEANUP_EN.md) — AWS budget and cleanup;
- [NOTICE_EN.md](NOTICE_EN.md) — authorship and license notice;
- [MODIFICATIONS_EN.md](MODIFICATIONS_EN.md) — educational-edition scope.

## Application capabilities

BookingKG supports registration and login, a destination catalog, search,
favorites, date availability, optional services, promo codes, booking creation
and cancellation, a personal trips page, and a printable voucher.

Real payments are not processed. The application is an educational workload.

## Start here

1. Read [PREREQUISITES_EN.md](PREREQUISITES_EN.md).
2. Read [ASSIGNMENT_EN.md](ASSIGNMENT_EN.md).
3. Create an implementation plan before writing infrastructure code.

Ready-made Docker, Kubernetes, Terraform, and GitHub Actions solution files are
intentionally not included. Never commit passwords, AWS keys, `.env`,
kubeconfig, Terraform state, or private keys.
