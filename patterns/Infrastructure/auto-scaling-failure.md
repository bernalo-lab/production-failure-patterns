# Pattern: Auto-Scaling Failure

## Description

An Auto-Scaling Failure occurs when systems fail to scale up or down appropriately in response to changing demand.

This creates either under-provisioning (causing incidents) or over-provisioning (causing unnecessary cost). In production, under-scaling is usually the dangerous failure mode.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Sudden latency spike during traffic increase
High CPU with no new instances
Queue depth growth
Increased error rates
Service saturation

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like code regression
Appears like database issue
Seems like dependency slowdown
Monitoring shows traffic normalisation later

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

Incorrect scaling thresholds
Broken scaling policies
Cloud provider quota limits
Delayed scaling response
Misconfigured health checks
Failed instance provisioning

---

# First Checks

Fast checks engineers should perform.

**Examples**:

scaling events
autoscaler logs
quota limits
provisioning failures
scaling thresholds
deployment timing

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

autoscaler activity logs
scaling metrics
CPU and queue depth graphs
cloud provisioning logs
failed instance launch events

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

autoscaling tests
better scaling thresholds
proactive scaling policies
quota monitoring
pre-warming critical services

---

<a href="../../categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>