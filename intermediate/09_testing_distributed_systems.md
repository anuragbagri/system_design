# Testing Strategies for Distributed Systems (Intermediate)

## Overview

Testing distributed systems requires a combination of unit, integration, contract, and chaos tests to exercise failure modes and guarantees.

## Test Types

- Unit tests and component tests
- Integration tests with test doubles or staging environments
- Contract tests (consumer-driven contracts)
- End-to-end tests for critical flows
- Chaos and fault-injection tests for resilience

## Practices

- Use lightweight test harnesses and mocks for fast feedback
- Maintain reproducible test environments (containers, infra as code)
- Test idempotency and retries explicitly
- Automate contract testing in CI

## Tooling

- Testcontainers, LocalStack for infra tests
- Pact for contract testing
- Chaos engineering tools (chaos-monkey, Litmus)

## Best Practices

- Keep tests deterministic and fast where possible
- Isolate flaky tests and fix root causes
- Use canary environments for risky changes

## References

- Consumer-driven contract testing resources
- Chaos engineering primer
