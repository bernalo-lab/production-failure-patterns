# Pattern: Missing Metrics for Critical Service

## Description

This pattern occurs when a critical production service lacks sufficient metrics to diagnose failures.

Without visibility into latency, error rates, request volume, or resource usage, engineers cannot quickly determine whether the service is healthy or failing.

This significantly slows incident response and often leads to guesswork during debugging.

---

## Typical Symptoms

**Examples**:

Service is failing but metrics show no anomalies
Limited dashboards available for the service
Engineers rely heavily on logs
Incident response requires manual investigation
Difficulty determining system behaviour

---

## Common Misleading Signals

**Examples**:

Looks like upstream service failure
Appears as network instability
Seems like database issue
Monitoring shows healthy services
Likely Root Causes

**Examples**:

Incomplete instrumentation
Metrics pipeline misconfiguration
Service deployed without observability standards
Missing application telemetry
Monitoring gaps after service refactor

---

## First Checks

**Examples**:

Check available metrics for service
Review service instrumentation
Inspect deployment configuration
Check monitoring dashboards
Review logging output

---

## Useful Signals

**Examples**:

Application logs
Infrastructure metrics
Container resource usage
Network latency metrics
Distributed traces

---

## Prevention

**Examples**:

Observability standards for services
Mandatory metrics instrumentation
Service health dashboards
Automated telemetry validation
Monitoring coverage reviews

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>