# API Gateway Patterns in Practice (Intermediate)

## Overview

API gateways act as a single entry point for clients, providing routing, authentication, rate-limiting, and API composition.

## Features

- Request routing and aggregation
- Authentication and authorization
- Rate limiting and quotas
- Caching and response shaping
- Protocol translation (HTTP ↔ gRPC)

## Deployment Models

- Centralized gateway vs decentralized (BFFs)
- Edge gateways vs regional gateways
- Sidecar proxies for service-level routing

## Best Practices

- Keep gateway logic minimal; delegate complex logic to backend services
- Use consistent authentication schemes (JWT/OIDC)
- Implement per-tenant and per-route rate limits
- Monitor gateway performance and error rates

## Tools

- Kong, Ambassador, Envoy, AWS API Gateway

## References

- API gateway pattern articles
