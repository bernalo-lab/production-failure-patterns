# Pattern: Zombie Leader Election

## Description

**Zombie Leader Election** happens when an old leader node continues acting as leader after leadership should have transferred, causing duplicate ownership and conflicting operations across distributed systems.

This often creates severe consistency issues in databases, schedulers, and orchestration platforms.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

duplicate scheduled job execution  
conflicting writes from multiple leaders  
unexpected lock contention  
stale node still processing traffic  
cluster instability after failover

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like scheduler duplication  
appears like network latency issue  
blamed on stale cache  
seems like orchestration bug  
appears as random application inconsistency

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

heartbeat failure detection delay  
network partition between nodes  
lease expiration handling bug  
clock drift affecting elections  
stale leadership state persistence

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify current leader ownership  
inspect lease expiration events  
review heartbeat and quorum status  
check old node activity logs  
confirm election transition timing

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

leader election logs  
lease renewal failures  
heartbeat monitoring events  
duplicate task execution traces  
cluster membership changes

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

strict lease expiration rules  
fencing and node isolation  
quorum-based elections  
clock synchronization controls  
leader handoff testing

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>