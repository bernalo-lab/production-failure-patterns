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

# 02. Pattern: feature-flag-meltdown

## Description

A <a href="../../patterns/operational/feature-flag-meltdown.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Feature Flag Meltdown**</a> occurs when enabling, disabling, or misconfiguring a feature flag causes unexpected system-wide impact.

This pattern appears in production systems because feature flags often control important code paths, traffic routing, backend calls, or expensive functionality. When a flag is rolled out too broadly or interacts badly with existing behaviour, it can trigger latency spikes, dependency overload, inconsistent behaviour, or partial outages.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>

