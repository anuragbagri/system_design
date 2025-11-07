# Kubernetes & Container Orchestration (Intermediate)

## Overview

Kubernetes is a container orchestration platform that automates deployment, scaling, and operation of containerized applications.

## Key Concepts

- Pods, Deployments, StatefulSets
- Services and Ingress
- ConfigMaps and Secrets
- Horizontal Pod Autoscaler
- Persistent Volumes

## Architecture

- Control plane (API server, scheduler, controller-manager)
- Worker nodes (kubelet, kube-proxy)
- etcd as cluster datastore

## Operational Considerations

- Resource requests/limits and QoS
- Pod disruption budgets and node draining
- Cluster autoscaling and multi-cluster setups
- Upgrade strategies and compatibilities

## Tooling

- kubectl, kustomize, helm
- Prometheus + Grafana for monitoring
- K9s, Lens for cluster troubleshooting

## Best Practices

- Define resource requests/limits to avoid noisy neighbors
- Use readiness/liveness probes
- Keep manifests declarative and use GitOps
- Secure cluster with RBAC and network policies

## References

- Kubernetes docs
