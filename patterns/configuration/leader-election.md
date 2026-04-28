# Pattern: Leader Election Failure

## Description

**Leader Election Failure** happens when distributed systems fail to correctly assign or maintain a single active leader responsible for coordination tasks.

This can create split-brain behaviour, stalled processing, or duplicate operations depending on whether no leader or multiple leaders emerge.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

duplicate job execution  
background workers stop processing  
split-brain database behaviour  
unexpected write conflicts  
cluster instability after failover

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like database corruption  
appears like queue backlog issue  
seems like network instability  
blamed on deployment changes  
appears as application logic bug

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

network partitions  
heartbeat failures  
clock drift between nodes  
consensus quorum issues  
incorrect failover configuration

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify current elected leader  
check quorum status  
inspect heartbeat health  
review recent failover events  
validate consensus system logs

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

leader election logs  
quorum metrics  
heartbeat timeout events  
cluster membership changes  
replication conflict logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

stable quorum design  
leader lease validation  
split-brain protection  
network partition handling  
election timeout tuning

---

<a href="../../categories/configuration/configuration.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
