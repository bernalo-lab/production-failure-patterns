# Pattern: Schema Migration Failure

## Description

A Schema Migration Failure occurs when database schema changes fail during deployment or introduce incompatibilities with running application versions.

In large distributed systems, schema migrations must be coordinated carefully. If migrations break compatibility or fail midway, applications may begin failing unexpectedly.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

application errors immediately after deployment
database query failures
missing columns or tables
inconsistent behaviour between services
increased error rates

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

appears like application bug
looks like database corruption
monitoring alerts from unrelated services
appears as sudden dependency failure

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

backward-incompatible schema change
partial migration deployment
failed migration script
version mismatch between services
schema replication delay

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify migration status
inspect database schema versions
check deployment logs
compare schema across replicas
review migration rollback plan

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

migration logs
database schema version tables
application error logs
deployment history
failed query logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

backward-compatible migrations
schema version control
staged migration rollouts
automated migration testing
rollback procedures

---

<a href="../../categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>