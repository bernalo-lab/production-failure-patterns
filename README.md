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
See available 'Infrastructure Failure Patterns' <a href="./categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

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

---

6. # Security & Access Failure Patterns
See available 'Security & Access Failure Patterns' <a href="./categories/security/security.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

These failures originate from authentication, authorisation, secrets management, certificates, and security controls that unintentionally disrupt system availability. They often appear as access denials, blocked traffic, expired credentials, or permission drift that causes production services to fail unexpectedly.

In many cases, the system is technically “healthy,” but users and services cannot operate because trust boundaries have broken.

**These are especially common in**:

IAM and access control systems
API gateways and authentication services
certificate and secret management
cloud security groups and firewalls
enterprise platforms with strict compliance controls

---

7. # Deployment & Release Failure Patterns
See available 'Deployment & Release Failure Patterns' <a href="./categories/deployment/deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

These failures occur during software releases, infrastructure changes, and CI/CD operations where deployment logic introduces instability into production. A small release issue can rapidly escalate into a widespread outage when rollback paths fail, versions become inconsistent, or infrastructure drifts from the expected state.

These incidents are often high-pressure because they happen during active change windows.

**These are especially common in**:

CI/CD pipelines
Kubernetes deployments
Terraform and Infrastructure as Code
blue-green and canary release strategies
multi-service microservice platforms

---

8. # Configuration & Control Plane Failure Patterns
See available 'Deployment & Release Failure Patterns' <a href="./categories/deployment/deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

These failures come from misaligned configuration, service discovery issues, stale caches, and failures inside the platform control plane that coordinates distributed systems.

They are particularly dangerous because they often create silent failures—systems appear healthy while behaviour becomes inconsistent across services, regions, or environments. Debugging is difficult because the problem is often hidden behind “correct-looking” infrastructure.

**These are especially common in**:

Kubernetes control planes
service discovery platforms
distributed systems coordination
environment management across dev/test/prod
cloud-native platforms with heavy automation

---

9. # Capacity & Performance Failure Patterns
See available 'Capacity & Performance Failure Patterns' <a href="./categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">here</a>

These failures emerge when systems gradually or suddenly exceed their operational limits, causing degradation before complete service failure. They often begin as latency spikes, queue growth, or resource contention and evolve into outages when autoscaling, storage, or compute cannot keep up with demand.

These are some of the most common causes of production instability at scale.

**These are especially common in**:

high-traffic APIs
queue and event-driven systems
databases and storage-heavy platforms
containerised workloads
large-scale cloud infrastructure environments

---

10.  # Business Logic & Workflow Failure Patterns

These failures occur when application workflows behave incorrectly even though infrastructure and monitoring may show everything as healthy. Problems like duplicate processing, broken retries, failed compensations, or inconsistent business states create serious operational and financial risk without obvious technical alerts.

These patterns are often the hardest to detect because they live inside business behaviour rather than system health metrics.

**These are especially common in**:

payment systems
insurance and financial platforms
order processing workflows
event-driven architectures
systems with asynchronous business processes


Real-world incident patterns are especially valuable.
