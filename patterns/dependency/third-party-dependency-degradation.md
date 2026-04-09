# Pattern: Third-Party Dependency Degradation

## Description

Third-Party Dependency Degradation occurs when an external service that your system relies on becomes slow, unstable, or partially unavailable.

Unlike a complete outage, the dependency still responds but with degraded performance or intermittent failures. Because the dependency technically remains available, systems often continue sending traffic, which can propagate latency and failures throughout the system.

This pattern frequently causes cascading latency across services that depend on the degraded system.

---

## Typical Symptoms

Engineers may observe:

Gradual latency increase across services
Increased error rates when calling external APIs
Slow responses from specific endpoints
Timeouts between internal services
Retry spikes
Thread pool exhaustion

---

## Common Misleading Signals

The issue may appear as:

Application performance regression
Infrastructure resource issues
Internal database slowdown
Network congestion

However, the root cause is often **performance degradation in a third-party dependency**.

---

## Likely Root Causes

Typical causes include:

External API performance issues
Third-party infrastructure overload
Regional outages affecting dependency providers
Dependency maintenance or deployment issues
Network routing problems

---

## First Checks

Engineers should check:

Latency metrics for dependency calls
Error rates from third-party APIs
Request timeout metrics
Dependency status pages
Recent traffic spikes to the dependency

---

## Useful Signals

Look for:

Dependency latency dashboards
Outbound request metrics
Timeout logs
Trace spans involving the dependency
Retry attempts

---

## Prevention

**Circuit Breakers**
Stop sending requests to degraded dependencies.

**Timeouts**
Ensure outbound requests have appropriate timeouts.

**Fallback Strategies**
Provide cached or degraded responses.

**Dependency Monitoring**
Track third-party health independently.

---

<a href="../../categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
