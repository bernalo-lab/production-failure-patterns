# Category: Observability & Operational Failure Patterns

---

# 01. Pattern: Bad Configuration Deployment

## Description

A <a href="../../patterns/operational/bad-configuration-deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Bad Configuration Deployment**</a> occurs when a configuration change introduces incorrect behaviour, instability, or service failure without requiring a code change.

This pattern appears in production systems because configuration often controls feature flags, connection settings, timeouts, resource limits, routing rules, and dependency endpoints. A small mistake in these settings can cause immediate and widespread impact, especially when rolled out across many instances at once.

---

# 02. Pattern: Feature Flag Meltdown

## Description

A <a href="../../patterns/operational/feature-flag-meltdown.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Feature Flag Meltdown**</a> occurs when enabling, disabling, or misconfiguring a feature flag causes unexpected system-wide impact.

This pattern appears in production systems because feature flags often control important code paths, traffic routing, backend calls, or expensive functionality. When a flag is rolled out too broadly or interacts badly with existing behaviour, it can trigger latency spikes, dependency overload, inconsistent behaviour, or partial outages.

---

# 03. Pattern: Monitoring Blind Spot

## Description

A <a href="../../patterns/operational/monitoring-blind-spot.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Monitoring Blind Spot**</a> occurs when a critical component, dependency, or behaviour is not being monitored or instrumented. As a result, failures occur without any alert or visible signal.

This pattern appears in production systems because observability coverage often evolves unevenly. New services, background jobs, third-party integrations, or infrastructure layers may be deployed without adequate monitoring.

When an issue occurs in these unmonitored areas, incident detection is delayed and engineers may only discover the problem through user reports or downstream failures.

---

# 04. Pattern: Alert Storm

## Description

An <a href="../../patterns/operational/alert-storm.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**alert-storm.md**</a> occurs when a single underlying issue triggers a large number of alerts across multiple systems.

This pattern appears in distributed systems where monitoring rules are configured independently for services, dependencies, and infrastructure layers. When one failure propagates through the system, each component generates its own alert.

The result is a flood of notifications that overwhelms responders and slows incident diagnosis.

---

# 05. Pattern: Missing Metrics for Critical Service

## Description

This pattern occurs when a <a href="../../patterns/operational/missing-metrics-critical-service.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**critical production service**</a> lacks sufficient metrics to diagnose failures.

Without visibility into latency, error rates, request volume, or resource usage, engineers cannot quickly determine whether the service is healthy or failing.

This significantly slows incident response and often leads to guesswork during debugging.

---

# 06. Pattern: Misleading Dashboard

## Description

A <a href="../../patterns/operational/misleading-dashboard.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Misleading Dashboard**</a> occurs when dashboards present incomplete, outdated, or incorrectly aggregated data that leads engineers toward the wrong diagnosis during an incident.

Dashboards often summarise complex system behaviour. When dashboards are poorly designed or rely on misleading metrics, they can hide real issues or suggest incorrect root causes.

---

# 07. Pattern: Logging Pipeline Failure

## Description

A <a href="../../patterns/operational/logging-pipeline-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Logging Pipeline Failure**</a> occurs when logs stop being collected, processed, or delivered to the logging system.

This removes one of the most important diagnostic tools during incidents. Engineers lose visibility into system behaviour and debugging becomes significantly harder.

---

# 08. Pattern: Trace Fragmentation

## Description

<a href="../../patterns/operational/trace-fragmentation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Trace Fragmentation**</a> occurs when distributed traces fail to connect across services.

Instead of a complete request path, engineers see partial traces, making it difficult to understand request flow during incidents.

---

# 09. Pattern: Alert Fatigue Masking Real Incident

## Description

<a href="../../patterns/operational/alert-fatigue-masking-real-incident.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Alert Fatigue**</a> occurs when engineers receive too many low-value alerts, causing them to ignore notifications or delay responses.

When a real incident occurs, it may be overlooked or dismissed because responders are accustomed to frequent false alarms.

---

# 10. Pattern: Incident Misclassification

## Description

<a href="../../patterns/operational/incident-misclassification.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Incident Misclassification**</a> occurs when an incident is incorrectly categorised during triage.

Incorrect classification can delay escalation, route the incident to the wrong team, or cause responders to pursue incorrect investigation paths.

---

# 11. Pattern: Time Synchronisation Drift

## Description

<a href="../../patterns/operational/time-synchronisation-drift.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Time Synchronisation Drift**</a> occurs when servers or services have inconsistent system clocks.

In distributed systems, time consistency is critical for logging, tracing, authentication, and coordination between services. When clocks drift apart, logs become misaligned and debugging becomes extremely difficult.

---

# 12. Pattern: Sampling Misconfiguration

## Description

<a href="../../patterns/operational/sampling-misconfiguration.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Sampling Misconfiguration**</a> occurs when observability systems sample too little or too much telemetry data.

When sampling is too aggressive, important diagnostic data may be lost. When sampling is too low, observability systems may become overloaded.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<< Back**</a>

