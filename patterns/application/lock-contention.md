# Pattern: Lock Contention

## Description

**Lock Contention** occurs when multiple processes, threads, or transactions compete for the same lock, causing work to block and throughput to fall.

This pattern appears in production systems when many operations target the same rows, keys, or shared resources at the same time. As lock wait times increase, requests become slower, queues form, and dependent services may begin to time out.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- Increased request latency
- Queue depth growth
- Blocked database transactions
- Throughput reduction
- Timeouts under moderate load
- Sudden slowdown on specific endpoints or operations

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like database performance issue
- Appears like application slowdown
- Monitoring alerts from downstream service
- Seems like CPU problem
- Appears like connection pool exhaustion

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- Multiple transactions updating the same data
- Long-running transactions
- Poor indexing causing broader locks
- Hot rows or keys
- Synchronous processing on shared state
- Increased concurrency on write-heavy paths

---

## First Checks

Fast checks engineers should perform.

Examples:

- Lock wait metrics
- Blocked transaction lists
- Slow query or transaction logs
- Hot tables or keys
- Recent changes to write patterns
- Concurrency level on affected endpoints

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- lock wait logs
- blocked transaction metrics
- slow transaction traces
- row or table lock statistics
- endpoint latency metrics
- database deadlock logs

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- shorter transactions
- improved indexing
- workload partitioning
- reduced contention on hot keys
- asynchronous processing
- lock-aware design