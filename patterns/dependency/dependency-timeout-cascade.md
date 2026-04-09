# Pattern: Dependency Timeout Cascade

## Description

Dependency Timeout Cascade occurs when one slow dependency causes multiple upstream services to experience timeouts.

These timeouts propagate through the call chain, eventually impacting many services.

---

## Typical Symptoms

Engineers may observe:

Increased request timeouts
Latency spikes
Cascading failures across services

---

## Common Misleading Signals

The issue may appear as:

Infrastructure overload
Network failure

---

## Likely Root Causes

Typical causes include:

Slow downstream services
Excessive request fan-out
Missing timeouts

---

## First Checks

Engineers should check:

Request latency across services
Dependency health
Timeout configuration

---

## Useful Signals

Look for:

Distributed traces
Timeout logs
Dependency latency metrics

---

## Prevention

**Timeouts**
Use strict timeout policies.

**Circuit Breakers**
Prevent cascading failures.

---

<a href="../../categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>