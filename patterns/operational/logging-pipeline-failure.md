# Pattern: Logging Pipeline Failure

## Description

A Logging Pipeline Failure occurs when logs stop being collected, processed, or delivered to the logging system.

This removes one of the most important diagnostic tools during incidents. Engineers lose visibility into system behaviour and debugging becomes significantly harder.

---

## Typical Symptoms

**Examples**:

Logs suddenly stop appearing
Missing logs during incident window
Delayed log ingestion
Incomplete logs for services
Logging dashboards empty

---

## Common Misleading Signals

**Examples**:

Appears like service stopped logging
Looks like application failure
Suggests infrastructure crash
Monitoring shows normal behaviour

---

## Likely Root Causes

**Examples**:

Logging agent crash
Log collector outage
Storage backend failure
Ingestion pipeline overload
Misconfigured logging configuration

---

## First Checks

**Examples**:

Check log collector health
Inspect logging agents
Review ingestion pipeline metrics
Verify log storage availability
Check recent configuration changes

---

## Useful Signals

**Examples**:

Logging infrastructure metrics
Ingestion pipeline throughput
Log collector logs
Storage service health
Infrastructure monitoring

---

## Prevention

**Examples**:

Redundant logging pipelines
Logging health alerts
Log ingestion monitoring
Logging agent health checks
Storage failover strategies

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>