# Pattern: Connection Pool Exhaustion

## Description

Connection Pool Exhaustion occurs when all available database or service connections are in use, preventing new requests from obtaining a connection.

Connection pools are used to limit the number of open connections to databases or external services.

When connections are held too long or requests increase suddenly, the pool may become depleted.

This causes requests to wait indefinitely or fail.

---

## Typical Symptoms

Common indicators include:

- Request timeouts
- Increased request latency
- Database connection wait errors
- Queue buildup in application servers
- Idle CPU with slow request processing

---

## Common Misleading Signals

This problem often appears as:

- Database performance issues
- Infrastructure resource limits
- Slow queries

However the real issue is **connection starvation**.

---

## Likely Root Causes

Typical causes include:

- Connections not being released properly
- Long-running database queries
- Slow transactions
- Incorrect pool size configuration
- Sudden traffic spikes

---

## First Checks

Engineers should inspect:

- Active vs idle connections
- Connection wait times
- Database transaction duration
- Application connection management
- Query performance metrics

---

## Useful Signals

Look for:

- Database logs showing connection wait events
- Application logs indicating connection timeout
- Increased request queue times

---

## Prevention

### Connection Timeouts

Prevent connections from being held indefinitely.

### Proper Connection Release

Ensure connections are returned to the pool.

### Pool Size Tuning

Adjust pool size based on workload.

### Query Optimisation

Reduce long-running database queries.

### Monitoring

Track connection pool metrics continuously.