# Pattern: Database Lock Contention

## Description

Database Lock Contention occurs when multiple transactions attempt to access the same database resources simultaneously and are forced to wait for locks to be released.

This pattern commonly appears in production systems during high concurrency workloads, poorly designed transaction boundaries, or when long-running transactions hold locks for extended periods. As contention increases, query latency rises and application throughput drops.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Sudden database latency increase
Slow or blocked queries
Application requests timing out
Spike in database wait events
Threads waiting on locks
Increased request queue depth

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Appears like database CPU saturation
Looks like infrastructure slowdown
Monitoring suggests database overload
Appears as random query latency spikes

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

Long-running transactions
Poor transaction design
Missing indexes forcing table scans
High concurrency on the same records
Row-level locks escalating to table locks
Batch jobs conflicting with live traffic

---

# First Checks

Fast checks engineers should perform.

**Examples**:

Identify blocking transactions
Check database lock wait metrics
Inspect slow query logs
Review transaction durations
Look for recent schema changes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

database lock wait metrics
blocked query logs
transaction duration metrics
database thread activity
slow query logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

shorter transactions
improved indexing strategy
row-level locking where possible
optimistic concurrency controls
workload separation for batch jobs

---

<a href="../../categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>