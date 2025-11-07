# Resilience Patterns

## Overview

Resilience patterns increase system robustness against failures and transient issues.

## Patterns

- Circuit Breaker
- Retry with exponential backoff and jitter
- Bulkhead isolation
- Bulkhead + thread pools
- Graceful degradation and fallback

## Design Considerations

- Failure detection and health checks
- Choosing timeouts and retry budgets
- Observability of failure modes

## Examples & Tools

- Hystrix (legacy), Resilience4j, Istio routing for isolation

## Best Practices

- Use bulkheads to isolate critical functionality
- Apply retries carefully to avoid amplifying load
- Monitor circuit state and set sensible thresholds

## References

- Patterns of Distributed Systems design literature
