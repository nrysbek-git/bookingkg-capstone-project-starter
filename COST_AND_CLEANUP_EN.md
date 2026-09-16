# AWS Budget and Cleanup

**Language:** [Русский](COST_AND_CLEANUP.md) · English

## Budget safety rule

Use only the training AWS account or sandbox and the Region approved by the
teacher. Before `terraform apply`, show the teacher the plan and estimated
cost. A personal payment card and a purchased domain are not project
requirements.

The EKS control plane, EC2 worker nodes, NAT Gateway, RDS, and Load Balancer
normally create the largest costs. Prices vary by Region and must be checked
against current official AWS Pricing before deployment.

## Before creating resources

- configure an AWS Budget and notifications when the sandbox allows it;
- use the smallest approved instance types;
- add the required `project`, `student`, `environment`, and `owner` tags;
- agree on a review time so infrastructure is not left idle;
- store Terraform state in the remote backend.

## During the project

```bash
terraform -chdir=terraform plan
kubectl get nodes
kubectl get service -A
aws sts get-caller-identity
```

Do not create duplicate clusters, NAT Gateways, RDS instances, or Load
Balancers to work around an error. Diagnose the existing resource first.

## Cleanup after the defense

1. Save approved evidence and workflow logs.
2. Delete Kubernetes resources that created external Load Balancers.
3. Confirm that the cloud Load Balancers have been removed.
4. Destroy infrastructure using the same state and variables:

   ```bash
   terraform -chdir=terraform plan -destroy
   terraform -chdir=terraform destroy
   ```

5. Check AWS Console or CLI for remaining EKS, EC2, RDS, NAT Gateway, Elastic
   IP, and Load Balancer resources.
6. Delete ECR images, logs, and the state bucket only according to course
   policy. Do not delete remote state until successful destroy is confirmed.

## Cleanup evidence

Record the cleanup date in `EVIDENCE.md` and attach safe confirmation without
account secrets. Never commit Terraform state or credential files.
