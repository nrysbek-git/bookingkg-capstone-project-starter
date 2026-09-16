# Grading Guide

**Language:** [Русский](GRADING_RUBRIC.md) · English

The 100-point scale and critical requirements are defined in
[ASSIGNMENT_EN.md](ASSIGNMENT_EN.md). This guide explains how the teacher
evaluates the result.

## Performance levels

The same principle applies to every category:

- **0%:** the component is missing or cannot run;
- **50%:** it works partially, was created manually, or is undocumented;
- **80%:** requirements are met with minor quality, security, or documentation issues;
- **100%:** the solution is reproducible, secure, documented, and understood by the student.

## Minimum, standard, and advanced

### Minimum — admission to the defense

- the application runs locally through Docker Compose;
- Terraform creates the main AWS infrastructure;
- images are stored in a private registry;
- frontend and backend run in Kubernetes;
- RDS is not exposed to the internet;
- the application is available through the AWS Load Balancer URL;
- Git contains no secrets.

Meeting the minimum does not guarantee a passing grade. The assignment points
and critical requirements still apply.

### Standard — expected result

- all required tasks are complete;
- CI/CD uses GitHub OIDC;
- deployments have two Ready replicas, probes, and resource limits;
- the teacher can reproduce deployment from the README;
- the student demonstrates rollout, rollback, and Pod recovery;
- cleanup is completed after review.

### Advanced — additional level

- custom domain and HTTPS;
- reusable Terraform modules;
- monitoring, centralized logging, or HPA;
- image scanning with a quality gate;
- backup restoration demonstration.

## Defense rules

1. The defense takes 20–30 minutes.
2. The student uses their own repository and commit history.
3. Screenshots support but do not replace a live demonstration.
4. The teacher selects at least two acceptance-criteria commands.
5. The student explains decisions in their own words; copying without
   understanding reduces the relevant score.
6. During a temporary cloud-provider outage, previously collected workflow
   logs, Terraform outputs, and evidence may be accepted.

## Academic integrity

Documentation, search engines, and AI tools may be used when course rules allow
it. The student remains responsible for the code and must explain every
resource, secret flow, and deployment step.
