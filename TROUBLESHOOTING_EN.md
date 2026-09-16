# Troubleshooting Guide

**Language:** [Русский](TROUBLESHOOTING.md) · English

This document provides diagnostic directions, not a completed implementation.

## Git and GitHub

### `Permission denied (publickey)`

```bash
git remote -v
ssh -T git@github.com
```

The remote must be a normal Git URL without Markdown brackets. GitHub does not
accept the account password for Git operations; use SSH or a Personal Access
Token according to course policy.

## Docker Compose

If the Docker daemon is unavailable, start Docker Desktop and run:

```bash
docker info
docker compose version
```

If a service never becomes healthy:

```bash
docker compose ps
docker compose logs database
docker compose logs backend
```

Check the healthcheck, database service hostname, environment variables, and
startup order. Inside Compose, `localhost` cannot address another container.

## Terraform and AWS

For `AccessDenied`, check the active identity, Region, and IAM permissions:

```bash
aws sts get-caller-identity
aws configure list
```

Do not expand a policy to `AdministratorAccess` without teacher approval. For a
state lock or backend error, confirm that no other apply is running before
changing the lock, S3 backend, or CI concurrency.

## Kubernetes

For `Pending`, `ImagePullBackOff`, or `CrashLoopBackOff`:

```bash
kubectl -n bookingkg get pods
kubectl -n bookingkg describe pod POD_NAME
kubectl -n bookingkg logs POD_NAME --previous
```

Inspect events, image URI/tag, ECR permissions, variables, Secret references,
probes, and database connectivity.

If a Service has no endpoints, compare selectors and Pod labels:

```bash
kubectl -n bookingkg get service,endpoints
kubectl -n bookingkg get pods --show-labels
```

If the Load Balancer takes a long time, inspect Service/Ingress events,
controller logs, subnet tags, security groups, and AWS quotas.

## Database

For connection failures, check the DNS hostname, port, database name, Secret,
security groups, and routing between EKS nodes and private RDS. Never expose a
password in terminal output, screenshots, or issues.

## Asking for help

Provide the task name, expected result, exact command, sanitized error, and
checks already performed. Never send AWS keys, passwords, kubeconfig, or
Kubernetes Secret contents.
