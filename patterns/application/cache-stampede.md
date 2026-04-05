# Pattern: Cache Stampede

## Description

A **Cache Stampede** occurs when many clients attempt to regenerate a cached value simultaneously after the cache entry expires.

Instead of one process rebuilding the cache while others wait, multiple processes attempt the same expensive operation.

This can overload databases, APIs, or backend systems.

The problem becomes severe in high-traffic environments where cache entries expire at the same moment.

---

## Typical Symptoms

Engineers may observe:

- Sudden **cache miss spike**
- Increased **database queries**
- CPU spikes on backend services
- Slow response times
- Increased latency following cache expiration

---

## Common Misleading Signals

The problem may look like:

- A database slowdown
- Unexpected traffic growth
- Backend service performance issues

However the real issue is **multiple processes rebuilding the same cache entry simultaneously**.

---

## Likely Root Causes

Common triggers include:

- Simultaneous cache expiration
- Missing cache locking
- High request volume
- Slow backend computation
- Insufficient cache TTL configuration

---

## First Checks

Engineers should check:

- Cache hit vs miss rate
- Cache TTL settings
- Backend query volume
- Cache key access patterns
- Database query logs

---

## Useful Signals

Look for:

- High number of identical backend queries
- Cache misses immediately followed by traffic spikes
- Increased request latency

---

## Prevention

### Cache Locking

Allow only one process to regenerate the cache.

### Early Cache Refresh

Refresh entries before expiration.

### Staggered Expiration

Use randomized TTL values.

### Background Cache Refresh

Refresh caches asynchronously.

### Request Collapsing

Serve pending requests with a shared response.

---

<a href="../../categories/application/application.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
