# Caching in System Design

## What is Caching?

Caching is the process of storing frequently accessed data in a fast-access storage layer to improve system performance and reduce load on primary data sources.

## Types of Caching

### 1. Application Cache

- **In-Memory Cache**
  - Stored in application memory
  - Fastest access
  - Limited by memory size
  - Examples: Memcached, Redis
- **Local Cache**
  - Cache within application
  - No network overhead
  - Limited to single instance
  - Examples: Guava Cache, Caffeine

### 2. Distributed Cache

- **Shared Cache**
  - Multiple applications access
  - Network overhead
  - Higher latency
  - Examples: Redis Cluster, Hazelcast
- **Replicated Cache**
  - Data replicated across nodes
  - High availability
  - Consistency challenges
  - Examples: Redis Sentinel, Memcached

### 3. CDN (Content Delivery Network)

- **Edge Caching**
  - Caches at edge locations
  - Reduced latency
  - Geographic distribution
  - Examples: Cloudflare, Akamai
- **Static Content**
  - Images, CSS, JS
  - Large files
  - High bandwidth savings

## Caching Strategies

### 1. Cache-Aside (Lazy Loading)

```
Application ---> Cache ---> Database
   ↑              |           |
   |              ↓           |
   |<------------[Cache Miss] |
   |                          |
   |<-------------------------|
```

- Application checks cache first
- Loads from DB if not found
- Updates cache after loading
- Pros:
  - Simple to implement
  - Flexible
  - No cache invalidation
- Cons:
  - Cache miss penalty
  - Stale data possible

### 2. Write-Through

```
Application ---> Cache ---> Database
   |              ↑           ↑
   |              |           |
   |<-------------|-----------|
```

- Write to cache and DB simultaneously
- Always consistent
- Higher write latency
- Pros:
  - Data consistency
  - No stale data
- Cons:
  - Higher write latency
  - More complex

### 3. Write-Behind (Write-Back)

```
Application ---> Cache ---> Database
   |              ↑           |
   |              |           |
   |<-------------|           |
   |                          |
   |<-------------------------|
```

- Write to cache first
- Asynchronously write to DB
- Better write performance
- Pros:
  - Better write performance
  - Reduced DB load
- Cons:
  - Data loss risk
  - Complex recovery

## Cache Eviction Policies

### 1. LRU (Least Recently Used)

- Evicts least recently accessed items
- Good for temporal locality
- Implementation:
  - Linked list
  - Hash map
  - O(1) operations

### 2. LFU (Least Frequently Used)

- Evicts least frequently accessed items
- Good for access patterns
- Implementation:
  - Min heap
  - Frequency counter
  - O(log n) operations

### 3. Time-Based

- TTL (Time To Live)
- Sliding window
- Fixed expiration
- Implementation:
  - Timestamp
  - Background cleanup
  - O(1) operations

## Cache Patterns

### 1. Multi-Level Cache

```
L1 Cache (Fastest) ---> L2 Cache ---> L3 Cache ---> Database
```

- Hierarchical caching
- Decreasing speed
- Increasing size
- Examples:
  - CPU cache hierarchy
  - Web browser cache
  - CDN hierarchy

### 2. Cache Invalidation

- **Time-based**
  - TTL expiration
  - Periodic refresh
- **Event-based**
  - Write invalidation
  - Update propagation
- **Manual**
  - Admin control
  - Emergency clearing

### 3. Cache Warming

- Pre-loading cache
- Strategies:
  - On startup
  - Scheduled
  - Predictive
- Benefits:
  - Reduced cold starts
  - Better performance
  - Smoother operation

## Best Practices

1. **Cache Size Management**

   - Monitor memory usage
   - Set appropriate limits
   - Implement eviction policies

2. **Cache Key Design**

   - Meaningful keys
   - Consistent format
   - Avoid collisions

3. **Cache Monitoring**

   - Hit/miss ratios
   - Latency metrics
   - Memory usage

4. **Error Handling**
   - Cache failures
   - Fallback strategies
   - Recovery procedures

## Real-world Examples

### 1. Facebook's TAO

- Distributed cache
- Social graph data
- High consistency
- Low latency

### 2. Twitter's Cache

- Multi-level caching
- Timeline data
- Real-time updates
- High throughput

### 3. Netflix's Cache

- CDN integration
- Video metadata
- Personalized content
- Global distribution

## Next Steps

1. Implement basic caching
2. Monitor cache performance
3. Optimize cache strategy
4. Scale cache infrastructure
