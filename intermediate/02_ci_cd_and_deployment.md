# CI/CD and Deployment Strategies (Intermediate)

## Overview

CI/CD automates building, testing, and deploying software. Deployment strategies control how new versions are released with minimal user impact.

## Common Deployment Strategies

- Blue/Green deployments
- Canary releases
- Rolling updates
- A/B testing

## CI/CD Pipeline Stages

- Build and compile
- Unit and integration tests
- Security and static analysis
- Staging deploy and smoke tests
- Production deploy with rollout strategy

## Tooling

- Jenkins, GitHub Actions, GitLab CI, CircleCI
- Argo CD, Flux for GitOps
- Helm, Kustomize for Kubernetes deployments

## Best Practices

- Keep pipelines fast and reliable; fail fast on regressions
- Automate rollbacks and health checks
- Use feature flags for incremental rollout
- Adopt GitOps for declarative deployments

## Observability

- Track deployment frequency, lead time, and change failure rate (DORA metrics)

## References

- DORA reports
- GitOps patterns
