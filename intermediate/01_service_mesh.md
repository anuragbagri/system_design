# Service Mesh (Intermediate)

## Overview

A service mesh is an infrastructure layer that handles service-to-service communication, typically via sidecar proxies. It provides traffic management, observability, security, and policy enforcement without changing application code.

## Core Capabilities

- Traffic routing and retries
- mTLS and service authentication
- Circuit breaking and rate limiting
- Telemetry (metrics, logs, traces)
- Policy enforcement and access control

## When to Use

- Large microservices deployments (many services)
- Need for centralized traffic control and observability
- Teams want out-of-process features without changing app code

## Trade-offs

- Adds operational complexity
- Increased resource usage (sidecars)
- Learning curve for control plane and policies

## Tools

- Istio, Linkerd, Consul Connect, Kuma

## Best Practices

- Start with a small subset of features (e.g., observability), then expand
- Use strict mTLS for production-critical services
- Monitor sidecar resource usage and tune limits
- Version control service mesh policies and test in staging

## References

- Istio documentation
- Linkerd docs
