# WhatsApp System Architecture: A Case Study

## Overview

WhatsApp is a globally scaled instant messaging system focused on low-latency, end-to-end encrypted messaging, presence, and media delivery for hundreds of millions of daily active users.

## Architecture Components

- Client apps (mobile and web)
- Edge servers and XMPP-based messaging frontends
- Message store and delivery system
- Media storage and CDN integration
- Presence and synchronization services
- End-to-end encryption (E2EE) key management
- Push notification integration for mobile

## Key Features

- End-to-end encryption for messages and calls
- Asynchronous delivery with store-and-forward for offline users
- Group messaging with membership and history sync
- Media transfer (images, voice notes, video) efficiently via CDN/storage

## Technical Implementation

- Messaging model: lightweight protocol (originally XMPP) with session affinity at edges.
- Store-and-forward: messages persisted until delivered and acked by clients.
- Media handling: clients upload media to storage, server returns a URL; clients fetch media with permission tokens; CDNs serve large files.
- E2EE: client-side key generation, server only routes encrypted payloads and stores encrypted blobs when necessary.
- Synchronization: sequence numbers and message queues to ensure ordering and de-duplication on reconnect.

## Challenges & Solutions

- Scale and fan-out in group messaging: use multicast-like techniques at the server to reduce duplication and optimize delivery.
- Data privacy: design so servers don't have plaintext access to message contents.
- Availability over poor networks: compact protocols, exponential backoff, and retry-stealing to reduce battery/network usage.
- Spam and abuse: rate limits, ML-based abuse detection, and reporting mechanisms.

## Observability & Resilience

- Monitor delivery latency, undelivered message queues, and presence propagation delays.
- Graceful degradation: allow reduced functionality on poor networks, fallback to SMS for registration.
- Use of regional edge clusters to reduce latency and meet data locality requirements.

## Best Practices

- Design protocols for minimal payload and efficient reconnection.
- Keep encryption primitives client-side where possible.
- Separate media delivery from control plane to optimize size and throughput.

## Lessons Learned

- Privacy-first designs change system trade-offs (e.g., less server-side visibility but stronger trust).
- Lightweight protocols and efficient fan-out are keys to scale at low cost.

## Future Considerations

- Multi-device synchronization improvements while preserving E2EE.
- Better spam/fraud detection without compromising privacy.
- Edge-based content moderation tooling that preserves privacy guarantees.
