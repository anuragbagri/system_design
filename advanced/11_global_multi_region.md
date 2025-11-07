# Global / Multi-region Design (Advanced)

## Overview

Designing for global scale requires balancing latency, availability, and consistency across regions. Multi-region architectures reduce latency and provide disaster resilience.

## Patterns

- Active-active vs active-passive replication
- Geo-partitioning and data locality
- Conflict resolution strategies (last-writer, CRDTs, application logic)

## Considerations

- Data sovereignty and compliance
- Cross-region replication lag and eventual consistency
- Traffic steering and DNS/Anycast strategies
- Failover automation and chaos testing across regions

## Tooling

- Global databases (Spanner, Cosmos DB), multi-region Kafka, CDN strategies

## Best Practices

- Partition write-heavy workloads by region where possible
- Use multi-region read replicas for lower-latency reads
- Design for eventual consistency where strict global consistency is not required

## References

- Google Spanner case studies
