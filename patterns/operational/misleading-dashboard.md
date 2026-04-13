# Pattern: Misleading Dashboard

## Description

A Misleading Dashboard occurs when dashboards present incomplete, outdated, or incorrectly aggregated data that leads engineers toward the wrong diagnosis during an incident.

Dashboards often summarise complex system behaviour. When dashboards are poorly designed or rely on misleading metrics, they can hide real issues or suggest incorrect root causes.

---

## Typical Symptoms

**Examples**:

Dashboards show healthy system despite failures
Conflicting metrics between dashboards
Delayed metric updates
Incorrect aggregation hiding spikes
Engineers relying on outdated panels

---

## Common Misleading Signals

**Examples**:

Normal system latency displayed
Low error rates despite user complaints
Infrastructure metrics appear healthy
Inconsistent values across dashboards

---

## Likely Root Causes

**Examples**:

Incorrect metric aggregation
Outdated dashboards
Missing service metrics
Incorrect dashboard queries
Data lag in monitoring pipeline

---

## First Checks

**Examples**:

Validate raw metrics
Compare multiple dashboards
Inspect monitoring query definitions
Verify metric time ranges
Confirm data freshness

---

## Useful Signals

**Examples**:

Raw metrics queries
Monitoring system logs
Trace data
Service latency metrics
Deployment timeline

---

## Prevention

**Examples**:

Dashboard review process
Observability design standards
Metric validation tests
Dashboard ownership policies
Regular monitoring audits

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>