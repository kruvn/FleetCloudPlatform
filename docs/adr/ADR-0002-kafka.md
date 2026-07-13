# ADR-0002: Apache Kafka as Event Streaming Platform

## Status

Accepted

---

# Context

The platform requires reliable high-throughput event processing.

Major event sources:

- Device telemetry
- Mission lifecycle
- System notifications
- Analytics streams

---

# Decision

Apache Kafka will be used as the primary event streaming platform.

---

# Reasons

## High Throughput

Kafka is designed for millions of events.

---

## Durability

Events are persisted and can be replayed.

---

## Scalability

Partitions allow horizontal scaling.

---

## Ecosystem

Kafka integrates well with:

- Monitoring tools
- Stream processing
- Data platforms

---

# Consequences

## Positive

- Reliable event processing
- Event replay capability
- Scalable consumers

---

## Negative

- Operational complexity
- Requires monitoring
- Requires partition strategy

---

# Alternatives Considered

## RabbitMQ

Rejected because the main requirement is event streaming rather than message queuing.

---

## Redis Streams

Rejected because it is not intended as the primary event backbone for this scale.

---

## Cloud managed solutions

Not selected initially because the project focuses on learning and demonstrating infrastructure ownership.