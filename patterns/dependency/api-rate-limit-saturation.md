# Pattern: API Rate Limit Saturation

## Description

API Rate Limit Saturation occurs when a system exceeds the allowed request quota imposed by a dependency or internal API.

When rate limits are exceeded, the dependency begins rejecting requests, typically with HTTP 429 responses.

This often triggers retries that worsen the situation.

---

## Typical Symptoms

Engineers may observe:

HTTP 429 responses
Increased retry traffic
Failed API requests
Spikes in outbound request attempts

---

## Common Misleading Signals

The issue may appear as:

Traffic spike
Dependency outage
Authentication issues

However, the system is actually being throttled by rate limits.

---

## Likely Root Causes

Typical causes include:

Traffic surges
Retry storms
Poor request batching
Misconfigured clients

---

## First Checks

Engineers should check:

429 response metrics
Retry configuration
Traffic patterns
Rate limit documentation

---

## Useful Signals

Look for:

HTTP 429 logs
Retry metrics
API usage dashboards

---

## Prevention

**Request Throttling**
Limit client request rates.

**Exponential Backoff**
Reduce retry intensity.

**Caching**
Avoid unnecessary API calls.

---

<a href="../../categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>