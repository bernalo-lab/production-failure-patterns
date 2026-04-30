# Pattern: Cross-Region Failover Split Brain

## Description

**Cross-Region Failover Split Brain** happens when two regions or clusters both believe they are the active primary after a failover event, causing conflicting writes, duplicate processing, and severe data inconsistency.

This is especially dangerous in active-active systems, disaster recovery environments, and globally distributed databases.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

duplicate writes across regions  
conflicting database records  
unexpected replication divergence  
inconsistent customer transactions  
simultaneous primary node ownership

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like database corruption  
appears like replication lag  
blamed on network instability  
seems like application race condition  
appears as isolated transaction failures

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

network partition during failover  
stale leader election state  
manual failover without coordination  
replication health false positive  
disaster recovery promotion drift

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify active primary ownership  
inspect failover event history  
check replication consistency status  
review leader election records  
confirm cross-region write paths

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

replication conflict logs  
leader election events  
database failover history  
cross-region write metrics  
split brain detection alerts

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

strong quorum-based failover  
fencing mechanisms  
automated split brain detection  
tested disaster recovery drills  
strict promotion controls

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>