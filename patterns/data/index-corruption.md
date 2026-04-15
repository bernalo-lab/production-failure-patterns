# Pattern: Index Corruption or Missing Index

## Description

Index Corruption or Missing Index occurs when database indexes become invalid, corrupted, or are missing entirely for critical queries.

Indexes are essential for efficient data retrieval. When they are corrupted or missing, the database may fall back to full table scans, dramatically increasing query latency and resource consumption.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden query latency spike
database CPU usage increase
large table scans appearing in query plans
slow response times for specific endpoints
database throughput degradation

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

appears like hardware performance issue
looks like traffic spike
seems like database capacity exhaustion
monitoring shows high CPU without clear cause

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

failed schema migration
corrupted index structures
missing indexes for new queries
accidental index removal
incomplete database restore
replication inconsistencies

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review query execution plans
check index health
inspect slow query logs
validate index presence
compare schema across environments

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

database execution plans
slow query logs
index usage metrics
database CPU metrics
schema change logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

schema migration validation
index monitoring
automated performance regression tests
schema drift detection
regular database maintenance

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>