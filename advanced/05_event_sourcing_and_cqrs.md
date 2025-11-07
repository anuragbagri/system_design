# Event Sourcing & CQRS

## Overview

Event sourcing persists state changes as an immutable sequence of events. CQRS separates read and write models to optimize each.

## Benefits

- Complete audit log and replayability
- Decoupled read models optimized for queries
- Easier temporal queries and debugging

## Challenges

- Event versioning and schema evolution
- Storage and retention management
- Eventual consistency between read and write models

## Design Patterns

- Event store (append-only) and snapshots
- Projection workers to build read models
- Idempotent command handling
- Sagas and orchestration for long-running transactions

## Tools & Examples

- EventStoreDB, Apache Kafka (as event log), custom stores

## Best Practices

- Design stable event schemas; use versioning
- Build resilient projection pipelines
- Provide monitoring for lag and failures

## References

- Event sourcing patterns
- Saga pattern for distributed transactions
