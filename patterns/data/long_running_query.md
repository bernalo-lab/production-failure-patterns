# Pattern: Long Running Query Saturation

## Description

Long Running Query Saturation occurs when one or more database queries take significantly longer than expected, consuming excessive resources (CPU, memory, locks, or I/O), which in turn degrades overall system performance.

In production systems, this pattern often emerges under load when inefficient queries, missing indexes, or large data scans block or delay other operations. Over time, these slow queries accumulate, leading to resource exhaustion and widespread latency across services that depend on the database.

This is especially common in large-scale systems where query complexity grows alongside data volume.

---

# Typical Symptoms

What engineers usually observe:

Gradual or sudden latency increase across services
Database CPU usage spikes
Increased query execution time
Connection pool exhaustion
Slow API responses or timeouts
Lock contention or blocked transactions
Queue buildup in services waiting on database responses

---

# Common Misleading Signals

Signals that often send engineers down the wrong path:

Appears like a general traffic spike
Looks like infrastructure or CPU scaling issue
Monitoring suggests downstream service latency
Interpreted as network latency between services
May resemble database outage rather than degradation

---

# Likely Root Causes

Typical reasons this pattern occurs:

Missing or inefficient database indexes
Full table scans on large datasets
Poorly written queries (e.g., nested joins, unbounded filters)
Sudden increase in data volume
Inefficient ORM-generated queries
Long-running reporting or batch queries competing with live traffic
Locking issues from large transactions

---

# First Checks

Fast checks engineers should perform:

Identify slow queries from database logs
Check query execution plans
Review recent schema or query changes
Inspect database CPU and I/O utilisation
Check for missing indexes on frequently queried fields
Analyse connection pool usage
Look for long-running transactions or locks

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue:

Slow query logs
Query execution time metrics
Database CPU and memory usage
Lock wait time metrics
Connection pool saturation metrics
Traces showing delays at database calls
Query plan analysis outputs

---

# Prevention

What can reduce the likelihood of this pattern:

Proper indexing strategy
Query optimisation and performance reviews
Use of pagination and bounded queries
Separation of OLTP and reporting workloads
Query timeouts and safeguards
Read replicas for heavy read workloads
Continuous monitoring of slow queries
Load testing with realistic data volumes

---

<a href="../../categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>