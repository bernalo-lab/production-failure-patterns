# Pattern: Partial Service Degradation

## Description

Partial Service Degradation occurs when a service continues operating but with reduced functionality or performance.

Instead of failing completely, certain operations fail while others remain available.

This often causes confusing symptoms during incident response.

---

## Typical Symptoms

Common observations include:

- Some API endpoints failing
- Increased latency for specific operations
- Intermittent errors
- Uneven performance across features

---

## Common Misleading Signals

This pattern may appear as:

- Random failures
- Network instability
- Client-side issues

However, the issue typically affects **specific components within the service**.

---

## Likely Root Causes

Typical causes include:

- Failing dependencies
- Resource exhaustion
- Feature-specific bugs
- Partial infrastructure failure

---

## First Checks

Engineers should verify:

- Which endpoints are affected
- Dependency health
- Resource metrics
- Feature flags

---

## Useful Signals

Useful indicators include:

- Endpoint-level error metrics
- Dependency-specific latency
- Request success ratios

---

## Prevention

### Graceful Degradation

Allow features to fail independently.

### Dependency Isolation

Avoid cascading failures.

### Feature Monitoring

Track health at endpoint level.

---

<a href="../../categories/application/application.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
