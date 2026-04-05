# Pattern: Dependency Cascade

## Description

A **Dependency Cascade** occurs when failure or slowdown in one service propagates through multiple dependent services, causing widespread system degradation.

Modern microservice architectures rely heavily on inter-service communication.

When one service becomes slow or unavailable, upstream services may block, retry, or fail — spreading the disruption throughout the system.

This cascading effect can rapidly transform a localized issue into a full system outage.

---

## Typical Symptoms

Engineers may observe:

- Increasing latency across services
- Error rates spreading between services
- Service timeouts
- Queue backlog growth
- Thread pool exhaustion

---

## Common Misleading Signals

The issue may appear as:

- Multiple unrelated service failures
- Network instability
- Infrastructure outage

But the real cause is usually **one failing dependency affecting others**.

---

## Likely Root Causes

Typical causes include:

- Slow downstream services
- Network latency
- Dependency outages
- Missing circuit breakers
- Aggressive retries

---

## First Checks

Engineers should verify:

- Which service failed first
- Dependency latency metrics
- Service dependency graphs
- Retry rates
- Timeout configurations

---

## Useful Signals

Metrics to inspect:

- Service latency per dependency
- Error propagation patterns
- Retry counts
- Timeout errors

Tracing tools are particularly useful for identifying cascading failures.

---

## Prevention

### Circuit Breakers

Stop calls to failing dependencies.

### Timeout Limits

Prevent long blocking requests.

### Bulkheads

Isolate service resources.

### Dependency Monitoring

Track health of critical dependencies.

### Graceful Degradation

Allow services to function partially when dependencies fail.