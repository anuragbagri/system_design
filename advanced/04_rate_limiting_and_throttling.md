# Rate Limiting & Throttling

## Overview

Rate limiting protects services from overload and enforces fair usage. Throttling shapes traffic to maintain stability.

## Techniques

- Token bucket and leaky bucket
- Fixed window and sliding window counters
- Distributed rate limiting (centralized vs local with synchronization)

## Policies

- Per-user, per-API-key, per-IP, per-tenant
- Burst handling and warm-up
- Quotas vs throttling

## Implementation Considerations

- Consistency and clock skew
- Performance of counters (Redis, in-memory, approximate algorithms)
- Client feedback (429 responses, retry-after headers)

## Use Cases

- Public APIs, login endpoints, write-heavy operations

## Best Practices

- Start with conservative limits and iterate
- Expose clear error codes and retry guidance
- Combine with authentication and abuse detection

## References

- Redis-based counting implementations
- API gateway rate limiting features
