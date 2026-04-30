# Pattern: Stale Disaster Recovery Environment Failure

## Description

**Stale Disaster Recovery Environment Failure** happens when a DR environment is outdated, misconfigured, or not aligned with production, causing failover to fail or behave incorrectly during an incident.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

failover environment not functioning  
missing services in DR  
configuration mismatches  
unexpected errors during failover  
data inconsistencies post-failover

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like failover script failure  
appears like infrastructure issue  
blamed on network configuration  
seems like deployment bug  
appears as incomplete recovery

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

DR environment not updated  
configuration drift  
untested failover process  
missing dependencies in DR  
inconsistent data replication

---

# First Checks

Fast checks engineers should perform.

**Examples**:

compare DR and production configs  
verify replication status  
review last DR test  
inspect missing services  
check failover logs

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

failover execution logs  
replication health metrics  
configuration drift reports  
DR environment health checks  
deployment history

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

regular DR testing  
configuration synchronization  
automated environment parity checks  
failover drills  
replication validation

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>