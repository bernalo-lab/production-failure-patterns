# Pattern: Database Connection Exhaustion

## Description

**Database Connection Exhaustion** occurs when the number of active database connections reaches the maximum allowed limit, preventing new requests from obtaining a connection.

This pattern appears in production systems when traffic spikes, queries run slowly, transactions remain open too long, or applications fail to release connections back to the pool. Once the connection limit is reached, application requests begin to queue, time out, or fail completely.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- Request timeouts
- Error rate increase
- Slow application responses
- Queue depth growth in web or worker tiers
- Database connection wait errors
- Healthy application servers with stalled requests

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like database crash
- Appears like network issue
- Monitoring alerts from downstream service
- Seems like slow query problem only
- Appears like general application slowdown

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- Connections not released properly
- Slow or long-running queries
- Traffic surge
- Oversized transaction duration
- Incorrect pool size configuration
- Retry storms increasing query load

---

## First Checks

Fast checks engineers should perform.

Examples:

- Active versus idle database connections
- Connection pool utilisation
- Slow query logs
- Transaction duration
- Application connection timeout settings
- Recent traffic changes

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- connection timeout logs
- active connection metrics
- database pool saturation metrics
- slow query logs
- transaction duration metrics
- request traces stalled on database access

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- connection pooling
- proper connection release
- query optimisation
- pool size tuning
- timeout controls
- database load testing

---
<a href="../../categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
