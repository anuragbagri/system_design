# Advanced Caching

## Overview

Beyond basic caching, advanced strategies improve hit rates, reduce staleness, and keep caches coherent across distributed environments.

## Patterns

- Multi-level caching (L1 in-process, L2 distributed)
- Cache partitioning (sharding)
- Cache-aside, write-through, write-back
- Hot-key mitigation (request coalescing, rate limiting)

## Consistency & Invalidation

- Time-to-live (TTL)
- Explicit invalidation using pub/sub
- Versioned keys and cache tags
- Background refresh and stale-while-revalidate

## Performance Considerations

- Size and eviction policies (LRU, LFU)
- Serialization cost and object shape
- Monitoring cache hit/miss and tail latencies

## Examples & Tools

- Redis, Memcached, Varnish, CDNs
- Client-side caching (service workers)

## Best Practices

- Cache on the critical read path
- Avoid caching highly dynamic, transactional data
- Monitor and tune TTLs and eviction policies

## References

- Redis docs
- Cache patterns literature
