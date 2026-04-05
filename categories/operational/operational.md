# Category: Observability & Operational Failure Patterns

---

# 01. Pattern: Bad Configuration Deployment

## Description

A <a href="../../patterns/operational/bad-configuration-deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Bad Configuration Deployment**</a> occurs when a configuration change introduces incorrect behaviour, instability, or service failure without requiring a code change.

This pattern appears in production systems because configuration often controls feature flags, connection settings, timeouts, resource limits, routing rules, and dependency endpoints. A small mistake in these settings can cause immediate and widespread impact, especially when rolled out across many instances at once.

---

# 02. Pattern: feature-flag-meltdown

## Description

A <a href="../../patterns/operational/bad-configuration-deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Feature Flag Meltdown**</a> occurs when enabling, disabling, or misconfiguring a feature flag causes unexpected system-wide impact.

This pattern appears in production systems because feature flags often control important code paths, traffic routing, backend calls, or expensive functionality. When a flag is rolled out too broadly or interacts badly with existing behaviour, it can trigger latency spikes, dependency overload, inconsistent behaviour, or partial outages.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>

