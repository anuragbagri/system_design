# Twitter (X) System Architecture: A Case Study

## Overview

Twitter (X) is a large-scale social platform delivering timelines, search, real-time notifications, and media to hundreds of millions of users — requiring low-latency fan-out and personalized ranking.

## Architecture Components

- Client apps and web frontend
- API gateway and edge caches
- Timeline generation pipeline (real-time and offline)
- Fan-out infrastructure for delivering tweets to followers
- Ranking/recommendation service
- Search/indexing service
- Media storage and CDN
- Analytics and stream processing pipelines

## Key Features

- High-cardinality fan-out for tweets (especially many followers)
- Real-time and offline timeline generation hybrid
- Personalized ranking using ML models
- Hashtag and full-text search, trends detection

## Technical Implementation

- Two main timeline models:
  - Fan-out on write for users with smaller follower lists
  - Fan-out on read (pull) for very large accounts
- Use of message queues and distributed logs (Kafka) to decouple producers and consumers.
- Real-time processing for notifications and push updates; batch recompute for heavy ranking.
- Indexing pipelines (Elasticsearch/Blob stores) for search and trends.

## Challenges & Solutions

- Fan-out storms from popular users: rate-limiting, hybrid fan-out strategies, and caching.
- Personalization at scale: separate feature extraction and model serving with low-latency caches.
- Abuse and spam: automated detection, human review, and throttling.

## Observability & Resilience

- Monitor fan-out latencies, timeline generation delays, and cache hit ratios.
- Backpressure and throttling on write paths to protect downstream workers.

## Best Practices

- Combine real-time and batch systems for correctness and cost efficiency.
- Use hybrid fan-out strategies to handle extremes in follower counts.
- Profile and optimize hot paths (timeline generation and ranking).

## Lessons Learned

- Design for extremes (celebrity accounts) as they drive most load patterns.
- Caching is essential but must be invalidated carefully to avoid stale timelines.

## Future Considerations

- More efficient ranking model serving at the edge.
- Improved personalization privacy controls and on-device ranking research.
