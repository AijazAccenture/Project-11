# Project 11: Infra Changes with Branching Policy

## Goal
Follow a branching strategy for infrastructure changes: no direct commits to `main`;
every change goes through a feature branch and a reviewed Pull Request.

## Branching strategy
| Branch | Purpose |
|---|---|
| `main` | Protected. Always valid. Changes only via Pull Request |
| `feature/<short-description>` | One branch per change, created from `main` |

## Workflow
1. Create a feature branch from `main`
2. Make the Terraform change, run `terraform fmt` and `terraform validate`
3. Push the branch and open a Pull Request into `main`
4. CI (Terraform fmt + validate) must pass
5. Review the PR, then merge and delete the feature branch

## Change log
| Version | Change |
|---|---|
| v1 | S3 bucket with versioning and tags (baseline) |
| v2 | Added CostCenter tag and cost_center variable (via feature branch + reviewed PR) |
