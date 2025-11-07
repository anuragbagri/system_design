# Distributed Transactions & Sagas (Advanced)

## Overview

Distributed transactions coordinate work across multiple services. The Saga pattern provides a pragmatic alternative to two-phase commit by implementing long-running transactions via a sequence of compensating actions.

## Patterns

- Two-Phase Commit (2PC): strong atomicity but blocking and complex
- Saga (choreography or orchestration): sequence of local transactions + compensations

## Design Considerations

- Idempotency of operations and compensations
- Ordering and partial failure handling
- Visibility into saga state and long-running workflows
- Monitoring and retry semantics

## Tools

- Temporal, Cadence, AWS Step Functions, custom orchestrators

## Best Practices

- Design compensating transactions carefully
- Keep transactions small and fast
- Provide observability for saga progress and failures

## References

- Saga pattern literature
- Temporal/Cadence documentation
