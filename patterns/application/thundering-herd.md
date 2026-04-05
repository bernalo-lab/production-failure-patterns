# Pattern: Thundering Herd

## Description

The **Thundering Herd** pattern occurs when a large number of clients or services simultaneously attempt to perform the same operation, overwhelming a system resource.

This often happens when multiple workers, services, or processes are waiting on the same trigger event — such as a cache expiration, lock release, or service recovery.

When the event occurs, all waiting entities wake up and attempt the operation at the same time, creating a sudden surge of traffic or computation.

In distributed systems, this can rapidly overload databases, caches, APIs, or storage layers.

---

## Typical Symptoms

Engineers often observe the following:

- Sudden **burst of identical requests**
- Rapid **CPU spike**
- **Database query surge**
- Cache miss rate increase
- Service latency spike
- Worker nodes waking simultaneously
- Lock contention or queue congestion

---

## Common Misleading Signals

The failure often appears as:

- A sudden **traffic spike**
- A **database performance problem**
- A **cache malfunction**
- Infrastructure capacity issue

In reality, the issue is caused by **synchronised behaviour across clients or workers**.

---

## Likely Root Causes

Typical triggers include:

- Cache expiration occurring simultaneously
- Worker processes polling at identical intervals
- Scheduled jobs triggering simultaneously
- Lock release allowing many waiting workers to proceed
- Recovery of a previously unavailable service

---

## First Checks

Engineers should quickly check:

- Cache expiration timing
- Worker polling intervals
- Scheduled job schedules
- Lock contention metrics
- Request burst patterns

---

## Useful Signals

Logs may reveal:

- Many identical requests within milliseconds
- Repeated access to the same resource

Metrics to inspect:

- Request rate spike
- Cache miss rate
- CPU utilisation
- Database query count

Tracing may show many concurrent requests targeting the same endpoint.

---

## Prevention

### Randomised Jitter

Add randomness to polling intervals or retry timing.

### Staggered Scheduling

Avoid running scheduled jobs at identical times.

### Request Coalescing

Ensure multiple identical requests are combined into one.

### Cache Warming

Preload caches before expiration events.

### Rate Limiting

Limit concurrent requests to critical services.

---

<a href="../categories/application/application.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;"><<Back</a>
