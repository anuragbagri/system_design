# Delivery Guarantees & Event Semantics (Advanced)

## Overview

Understanding delivery guarantees (at-most-once, at-least-once, exactly-once) and how to achieve them is crucial in distributed and streaming systems.

## Guarantees

- At-most-once: no retries, possible data loss
- At-least-once: retries may cause duplicates; requires idempotency
- Exactly-once: hard to achieve, often implemented via transactional sinks or deduplication

## Techniques

- Idempotent operations and deduplication keys
- Consumer offsets and transactional writes (Kafka Transactions)
- Exactly-once semantics via two-phase commit or atomic sinks

## Trade-offs

- Performance vs correctness
- Complexity of implementation vs business need

## Best Practices

- Prefer idempotency and deduplication for resilience
- Use transactional features of the messaging system for critical paths
- Monitor and handle poison messages and dead-letter queues

## References

- Kafka transactions and exactly-once guides
