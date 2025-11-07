# Serverless Architectures (Intermediate)

## Overview

Serverless lets you run functions or managed services without operating servers. It shifts operational tasks to the cloud provider and enables rapid scaling and pay-per-use billing.

## Models

- Functions as a Service (FaaS): AWS Lambda, Azure Functions
- Backend as a Service (BaaS): managed databases, auth, messaging

## Benefits

- Reduced operational burden
- Cost-effective for spiky workloads
- Fast developer productivity

## Trade-offs

- Cold starts and latency
- Limited execution time and resource limits
- Vendor lock-in and observability challenges

## Design Considerations

- Idempotency and retries
- Fan-out limits and concurrency control
- Managing state (external stores, durable services)

## Best Practices

- Keep functions small and single-purpose
- Use async patterns for long-running workflows (Step Functions)
- Monitor cold start frequency and optimize packaging

## References

- Provider docs (AWS Lambda, Azure Functions, GCP Cloud Functions)
