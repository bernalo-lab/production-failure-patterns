# Pattern: Downstream Retry Amplification

## Description

Downstream Retry Amplification occurs when retry mechanisms multiply traffic toward failing services.

Instead of reducing failure impact, retries create additional load that worsens the problem.

---

## Typical Symptoms

Engineers may observe:

Sudden traffic spikes
Increased dependency load
Retry storms
Cascading service failures

---

## Common Misleading Signals

The issue may appear as:

DDoS attack
Traffic surge
Infrastructure overload

---

## Likely Root Causes

Typical causes include:

Aggressive retry policies
Missing exponential backoff
Multiple retry layers

---

## First Checks

Engineers should check:

Retry configuration
Request retry counts
Downstream error rates

---

## Useful Signals

Look for:

Retry metrics
Outbound request spikes
Dependency error logs

---

## Prevention

**Exponential Backoff**
Reduce retry intensity.

**Retry Budgets**
Limit retries during incidents.

**Circuit Breakers**
Stop retrying failing services.

---

<a href="../../categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>