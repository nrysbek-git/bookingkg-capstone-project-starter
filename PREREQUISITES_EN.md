# Capstone Prerequisites

**Language:** [Русский](PREREQUISITES.md) · English

## Intended audience

This project follows the first-semester foundations and the main infrastructure
topics of the second semester. Students do not need to write frontend or
backend business logic; their task is to build a reproducible DevOps process.

## Required knowledge

Before starting, a student should be able to:

- use a Linux or macOS terminal and understand paths, permissions, and processes;
- use Git branches, commits, pull requests, merges, and `.gitignore`;
- explain IP addresses, ports, DNS, HTTP/HTTPS, and private/public subnets;
- read a Dockerfile and run containers;
- use environment variables without storing secrets in Git;
- read YAML and understand basic Kubernetes resources;
- run basic PostgreSQL queries;
- explain IAM and the principle of least privilege.

## Required tools

- Git and a GitHub account;
- Docker Desktop or Docker Engine with Compose;
- AWS CLI v2 and a training AWS account or sandbox;
- Terraform;
- `kubectl`;
- a text editor such as VS Code;
- Helm (optional).

Verify the environment:

```bash
git --version
docker --version
docker compose version
aws --version
terraform version
kubectl version --client
```

## Access requirements

Before the cloud part, the teacher must confirm:

- the AWS Region and training-account restrictions;
- available quotas and budget;
- the GitHub repository for the project;
- whether a training subdomain is provided;
- whether each student receives an EKS cluster or uses a shared cluster.

Students are not required to buy a domain or use a personal payment card.

## Readiness check

A student is ready when they can independently:

1. clone a repository and create a branch;
2. run a simple container;
3. explain the browser → frontend → backend → database request path;
4. sign in to the training AWS account without exposing credentials;
5. name the command that removes Terraform-managed infrastructure.
