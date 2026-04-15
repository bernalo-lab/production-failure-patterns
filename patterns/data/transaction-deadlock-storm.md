# Pattern: Transaction Deadlock Storm

## Description

A Transaction Deadlock Storm occurs when multiple transactions hold locks that block each other in a circular dependency, causing the database to abort transactions repeatedly.

When deadlocks occur frequently, systems may experience retries, increased latency, and cascading service degradation.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden spike in transaction failures
database deadlock errors
retry storms in application logs
increased request latency
database CPU increase

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

appears like application bug
looks like database overload
resembles network timeout issues
seems like concurrency problem in application logic

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

inconsistent transaction ordering
long-running transactions
high concurrency updates on shared records
missing indexes increasing lock duration
batch jobs colliding with live traffic

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review database deadlock logs
analyse transaction ordering
inspect blocking queries
identify conflicting queries
check retry behaviour in services

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

deadlock logs
transaction failure metrics
retry counts in application logs
database lock graphs
slow query metrics

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

consistent transaction ordering
smaller transactions
reduced lock scope
database deadlock monitoring
retry backoff strategies

---

<a href="../../categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>