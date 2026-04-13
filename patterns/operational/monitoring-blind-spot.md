# Pattern: Monitoring Blind Spot

## Description

A Monitoring Blind Spot occurs when a critical component, dependency, or behaviour is not being monitored or instrumented. As a result, failures occur without any alert or visible signal.

This pattern appears in production systems because observability coverage often evolves unevenly. New services, background jobs, third-party integrations, or infrastructure layers may be deployed without adequate monitoring.

When an issue occurs in these unmonitored areas, incident detection is delayed and engineers may only discover the problem through user reports or downstream failures.

---

## Typical Symptoms

What engineers usually observe.

**Examples**:

Users report errors before monitoring detects problems
Partial outages with no alerts triggered
Unexpected service degradation without visible metrics
Missing telemetry for a specific service or dependency
Delayed incident detection

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like a frontend bug
Appears as intermittent user issues
Seems like network instability
No alerts triggered despite real failure
Monitoring dashboards appear normal

---

## Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

Missing instrumentation for new service
Critical dependency not included in monitoring scope
Observability configuration drift
Background jobs without metrics
Alerting rules missing for important signals

---

## First Checks

Fast checks engineers should perform.

**Examples**:

Verify monitoring coverage for affected service
Check recent deployments introducing new components
Review logs for services lacking metrics
Inspect observability configuration changes
Confirm dependency monitoring exists

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

Raw service logs
Infrastructure metrics
Network telemetry
Application traces
Deployment change logs

---

## Prevention

What can reduce the likelihood of this pattern.

**Examples**:

Observability coverage audits
Monitoring templates for new services
Instrumentation standards
Service health checks
Automated alert rule generation

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>