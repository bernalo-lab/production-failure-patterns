# Pattern: Thread Pool Exhaustion

## Description

Thread Pool Exhaustion occurs when all available worker threads in a service become occupied, preventing new requests from being processed.

Most application servers and frameworks use thread pools to manage concurrency.

If threads become blocked — waiting for slow operations such as database calls or external APIs — the pool can fill up quickly.

Once exhausted, incoming requests must wait or fail.

---

## Typical Symptoms

Common indicators include:

- Request queue growth
- High request latency
- Timeout errors
- Low CPU usage despite high latency
- Thread pool utilisation at 100%

---

## Common Misleading Signals

This issue often appears as:

- Application performance degradation
- Database issues
- Network latency

But the underlying problem is **blocked worker threads**.

---

## Likely Root Causes

Typical causes include:

- Slow database queries
- Blocking network calls
- Long-running computations
- Poor timeout configuration
- Dependency slowdown

---

## First Checks

Engineers should inspect:

- Thread pool metrics
- Active vs idle threads
- Dependency latency
- Request duration
- Queue depth

---

## Useful Signals

Helpful indicators include:

- Thread dump analysis
- Long-running request logs
- High request waiting times
- Service dependency delays

---

## Prevention

### Asynchronous Processing

Avoid blocking threads during I/O.

### Thread Pool Monitoring

Track thread pool health metrics.

### Timeout Controls

Prevent long blocking operations.

### Load Shedding

Reject excess requests under load.

### Bulkhead Isolation

Separate critical tasks into different thread pools.