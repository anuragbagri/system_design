# Gmail System Architecture: A Case Study

## Overview

Gmail is a large-scale email service that handles billions of messages, delivering mail reliably, providing search, spam filtering, and integrations with other services.

## Architecture Components

- Client frontends (web, mobile)
- Mail ingestion and SMTP gateways
- Mail storage and indexing (user mailboxes)
- Search and indexing service
- Spam and abuse detection pipelines (ML)
- Attachment storage and CDN
- Delivery and retry mechanisms

## Key Features

- Near-instant delivery and rich search over mail history
- Spam filtering and phishing detection
- Conversation threading and labels
- Offline access and synchronization

## Technical Implementation

- Store messages in distributed storage with per-user indexing for fast queries.
- Inverted indexes and document stores (custom indexing) for search.
- Spam detection: multi-stage filters, heuristics, and ML models trained on signals.
- Attachment handling: deduplication, chunked uploads, and CDNs for large files.

## Challenges & Solutions

- High write volume and inbox churn: append-only stores with compacted indices.
- Search latency across huge histories: sharded indexes and per-user caches.
- Spam/abuse evolving constantly: continuous model retraining and feature engineering.

## Observability & Resilience

- Track delivery latencies, bounce rates, and spam false positives.
- Retries and backoff for transient mail delivery failures.

## Best Practices

- Use append-only logs for message durability and easier replication.
- Separate indices per user to localize queries and improve performance.
- Invest in automated model pipelines for spam detection.

## Lessons Learned

- Indexing at scale requires careful sharding and compaction strategies.
- Robust spam detection is essential to preserve user trust.

## Future Considerations

- More privacy-preserving filtering techniques.
- Improved offline search and client-side indexing options.
