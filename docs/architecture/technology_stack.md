# Technology Stack

## Overview

This document describes the initial technology choices for Fleet Cloud Platform.

The selected technologies are based on the following principles:

- High scalability
- Cloud-native approach
- Production-proven solutions
- Strong ecosystem support
- Observability and maintainability
- Suitability for event-driven distributed systems

Technology choices may evolve as the platform grows.

---

# Backend

## .NET

Version:

.NET 9+

Purpose:

Main application runtime.

Reasons:

- High performance
- Mature ecosystem
- Excellent support for distributed systems
- Strong tooling
- Native support for cloud environments

---

## ASP.NET Core

Purpose:

Building HTTP APIs and backend services.

Usage:

- REST APIs
- Internal service communication
- Health endpoints
- Middleware pipeline

---

## gRPC

Purpose:

Internal communication between services.

Usage:

- Low latency service-to-service communication
- Strong contracts
- High performance

---

# Architecture Style

## Event-Driven Architecture

Primary communication pattern between services.

Reasons:

- Loose coupling
- Horizontal scalability
- Asynchronous processing
- Better fault isolation

Main event broker:

Apache Kafka

---

## Domain Driven Design

The system will follow DDD principles.

Main concepts:

- Bounded Contexts
- Aggregates
- Domain Events
- Ubiquitous Language

---

## CQRS

Command Query Responsibility Segregation will be used where it provides value.

Commands:

Change system state.

Queries:

Read optimized data.

---

# Messaging

## Apache Kafka

Purpose:

Central event streaming platform.

Usage:

- Telemetry streams
- Domain events
- Async communication
- Event replay

---

# Databases

## PostgreSQL

Purpose:

Transactional data storage.

Usage:

- Fleet data
- Users
- Missions
- Configuration
- Billing information

---

## ClickHouse

Purpose:

Analytical storage.

Usage:

- Telemetry analytics
- Time-series queries
- Aggregations
- Reporting

---

## Redis

Purpose:

Fast in-memory storage.

Usage:

- Caching
- Distributed locks
- Short-lived state
- Rate limiting

---

# Observability

## OpenTelemetry

Purpose:

Unified telemetry collection.

Provides:

- Logs
- Metrics
- Distributed tracing

---

## Prometheus

Purpose:

Metrics collection.

Examples:

- Request latency
- Kafka lag
- Event processing rate

---

## Grafana

Purpose:

Visualization.

Dashboards:

- Fleet health
- System metrics
- Business metrics

---

## Loki

Purpose:

Centralized log aggregation.

---

## Tempo

Purpose:

Distributed tracing storage.

---

# Infrastructure

## Docker

Purpose:

Local development environment.

---

## Kubernetes

Purpose:

Container orchestration.

Future usage:

- Service deployment
- Scaling
- Self-healing
- Rolling updates

---

## CI/CD

Planned tools:

- GitHub Actions

Purpose:

- Build automation
- Testing
- Deployment pipelines

---

# Development Principles

Technology decisions should always support:

- Scalability
- Reliability
- Maintainability
- Observability
- Evolution of the platform