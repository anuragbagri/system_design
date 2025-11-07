# Stream Processing

## Overview

Stream processing handles continuous data flows with low-latency processing and stateful transformations.

## Models

- Stateless transformations (map/filter)
- Stateful processing (windowed joins, aggregations)
- Exactly-once vs at-least-once delivery semantics

## Frameworks & Tools

- Apache Flink, Kafka Streams, Apache Beam, Spark Structured Streaming

## Design Considerations

- State backend and checkpointing
- Event time vs processing time and watermarking
- Scaling and partitioning

## Use Cases

- Real-time analytics, fraud detection, streaming ETL

## Best Practices

- Use durable state stores and backups
- Choose processing guarantees according to correctness needs
- Monitor throughput, latency, and checkpoint durations

## References

- Flink and Kafka Streams documentation
