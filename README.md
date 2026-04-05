# Production Failure Patterns
A field guide for SREs, DevOps engineers, and incident responders.

A growing library of real production failure patterns engineers encounter in distributed systems.

The goal is simple:

Help engineers recognise failure modes faster during incidents.

When systems fail, teams often lose time chasing the wrong hypothesis.

Pattern recognition dramatically accelerates debugging.

---

## What is included

Each pattern describes:

- Typical symptoms
- Misleading signals
- Likely root causes
- First checks to perform
- Useful observability signals
- Prevention strategies

---

## Why this exists

Most incident response knowledge is buried inside companies.

This repository aims to document common patterns engineers face in real production systems.

These patterns appear repeatedly across:

- cloud infrastructure
- microservices architectures
- distributed systems
- large scale platforms

---

## Current Categories

1. # Application Failure Patterns
See available 'Application Failure Patterns' <a href="./categories/application/application.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

Application Failure Patterns occur within the behaviour or runtime logic of services and applications.

These failures typically arise from how applications handle requests, concurrency, retries, caching, or resource management. While the underlying infrastructure may be healthy, application-level design or configuration decisions can cause cascading issues under load.

Common examples include retry storms, cache stampedes, thread pool exhaustion, and memory leaks. These patterns often appear during traffic spikes, dependency slowdowns, or inefficient resource handling.

Recognising application failure patterns helps engineers diagnose problems faster by focusing on runtime behaviour and service interaction, rather than immediately assuming infrastructure faults.

---

2. # Infrastructure Failure Patterns
See available 'Infrastructure Failure Patterns' <a href="./categories/Infrastructure/Infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

Infrastructure Failure Patterns occur when underlying platform components such as compute resources, networking, storage devices, or load balancers become constrained or unavailable.

These failures affect the environment in which applications run, often leading to widespread system instability. Typical triggers include CPU starvation, disk I/O saturation, network partitions, or load balancer overload.

Because infrastructure components support many services simultaneously, these failures can cause system-wide performance degradation.

Understanding infrastructure failure patterns helps engineers quickly identify when issues originate from the platform layer rather than the application layer.

---

3. # Data & Storage Failure Patterns
See available 'Data & Storage Failure Patterns' <a href="./categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

Data & Storage Failure Patterns arise when databases, storage systems, or data pipelines experience contention, capacity limits, or replication issues.

Modern systems rely heavily on persistent data stores. When these systems degrade, applications may encounter slow queries, connection exhaustion, replication lag, or lock contention.

These failures are particularly challenging because they may cause partial system failures, inconsistent data views, or degraded performance across multiple services.

Recognising data-layer failure patterns allows engineers to focus on query performance, connection management, and storage throughput during incident investigation.

---

4. # Dependency Failure Patterns
See available 'Dependency Failure Patterns' <a href="./categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

Dependency Failure Patterns occur when external or internal services that an application relies on become slow, unavailable, or unstable.

In distributed systems, most services depend on multiple downstream components such as APIs, databases, authentication services, or third-party providers. When one of these dependencies degrades, the impact can propagate upstream, causing cascading failures.

Typical patterns include dependency cascades, timeout amplification, and retry storms triggered by failing services.

Understanding dependency failure patterns helps teams design systems with circuit breakers, timeouts, and graceful degradation to reduce the impact of failing components.

---

5. # Observability & Operational Failure Patterns
See available 'Observability & Operational Failure Patterns' <a href="./categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

Observability & Operational Failure Patterns occur when system visibility, configuration management, or operational processes fail during incidents.

These failures do not always originate from application code or infrastructure. Instead, they arise from missing telemetry, incorrect configuration changes, or operational mistakes.

Examples include bad configuration deployments, feature flag failures, incomplete monitoring coverage, and misleading alert signals.

Recognising these patterns helps teams improve incident detection, troubleshooting workflows, and operational resilience, ensuring that engineers can respond effectively during production failures.

---

## Part of the Incident Engineering Knowledge Base

This repository is part of a broader effort to document production failure patterns and debugging strategies.

---

## Contributions

Engineers are welcome to contribute additional patterns.

Real-world incident patterns are especially valuable.
