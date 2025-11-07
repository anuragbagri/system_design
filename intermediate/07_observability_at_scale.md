# Observability Patterns at Scale (Intermediate)

## Overview

Observability at scale focuses on collecting, storing, and correlating telemetry (logs, metrics, traces) across many services while controlling cost and retention.

## Challenges

- High cardinality metric explosion
- Large log volumes and storage costs
- Trace sampling strategies and correlation

## Strategies

- Sampling and adaptive retention
- Aggregation and rollups for long-term metrics
- Correlate traces, logs and metrics via trace IDs and tags
- Use distributed tracing selectively for high-value paths

## Tooling

- Prometheus + Thanos, Cortex for long-term metrics
- OpenTelemetry for traces
- ELK/Loki for logs

## Best Practices

- Define high-value traces and sample others
- Use structured logs and consistent tagging
- Implement cost-aware retention policies

## References

- OpenTelemetry guidance
- Prometheus + Thanos patterns
