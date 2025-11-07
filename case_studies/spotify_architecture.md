# Spotify System Architecture: A Case Study

## Overview

Spotify is a large-scale music streaming service delivering low-latency playback, personalized recommendations, and playlist management for millions of users.

## Architecture Components

- Client apps (mobile, desktop, web)
- Content ingestion and transcoding pipeline
- CDN and edge caches for music files
- Metadata services (catalog, playlists, user libraries)
- Recommendation and personalization services (ML)
- Playback orchestration and offline sync
- Licensing and rights management

## Key Features

- Adaptive streaming and cached offline playback
- Real-time recommendation and playlist personalization
- Large catalog indexing and search
- Rights- and region-based content filtering

## Technical Implementation

- Music files stored in object storage and served via CDN; tile-based chunking for efficient seeks.
- Hybrid recommendation: offline batch models for candidate generation and online models for ranking.
- Use of event streams (Kafka) to capture user actions for near-real-time features.
- Offline sync: deterministic download and local cache management on devices.

## Challenges & Solutions

- Ensuring smooth playback with low startup latency: prefetching and aggressive edge caching.
- Personalization at scale: feature pipelines, candidate generation, and low-latency ranking.
- Licensing constraints per region: dynamic content gating and legal metadata.

## Observability & Resilience

- Monitor playback startup times, buffer underruns, CDN availability.
- Graceful fallback to lower-bitrate streams during congestion.

## Best Practices

- Separate control (catalog metadata) and data (media files) planes.
- Use streaming telemetry to feed recommendation models.
- Provide deterministic behavior for offline playback to avoid licensing issues.

## Lessons Learned

- Offline-first UX increases user retention but complicates sync and storage management.
- Decoupling recommendation pipelines helps scale model experimentation without impacting playback.

## Future Considerations

- On-device ranking to reduce latency and privacy exposure.
- Smarter edge caching tuned to personalized tastes.
