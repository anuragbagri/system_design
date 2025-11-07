# Consistency Models

## Overview

Consistency models describe guarantees about visibility and ordering of updates in distributed systems. Choosing the right model affects correctness, latency, and availability.

## Common Models

- Strong consistency (linearizability)
- Sequential consistency
- Causal consistency
- Eventual consistency

## Trade-offs (CAP & PACELC)

- Availability vs consistency during partitions (CAP)
- Latency vs consistency during normal operation (PACELC)

## Design Considerations

- Use-case requirements (finance vs social feed)
- Read/write patterns and quorum configuration
- Conflict resolution (last-write-wins, CRDTs, application logic)
- Client-side vs server-side enforcement

## Examples

- Distributed databases: Spanner (strong), Cassandra (eventual), Dynamo-style quorum systems
- CRDTs for offline-first apps

## Best Practices

- Document consistency guarantees in APIs
- Use versioning and idempotency for updates
- Prefer causal or strong consistency when correctness is critical

## References

- CAP theorem
- PACELC model
