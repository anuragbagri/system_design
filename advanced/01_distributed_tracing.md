# Distributed Tracing

## Overview

Distributed tracing records the flow of requests across services, capturing timing and causal relationships. It helps identify latency sources and pinpoint failures in complex microservice architectures.

## Key Concepts

- Trace, span, and span context
- Sampling strategies
- Trace propagation (headers)
- Correlation IDs

## When to use

- Microservices-based systems
- High latency or opaque failure modes
- Complex distributed transactions

## Design Considerations

- Instrumentation (manual vs automatic)
- Sampling rates and overhead
- Storage and retention of traces
- Privacy and sensitive data redaction

## Tools & Examples

- Jaeger, Zipkin, OpenTelemetry
- Instrumentation libraries for Java, Python, Node.js

## Best Practices

- Start with low-overhead sampling
- Instrument critical paths first
- Correlate traces with logs and metrics
- Use OpenTelemetry for portability

## References

- OpenTelemetry project
- Jaeger documentation
