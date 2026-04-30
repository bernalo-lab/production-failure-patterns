# Pattern: Leap Second Failure

## Description

**Leap Second Failure** happens when systems fail to correctly handle the insertion of an extra second in UTC timekeeping, causing time calculations, scheduling, and distributed coordination to behave unpredictably.

This can trigger outages in databases, schedulers, authentication systems, and distributed clusters that depend heavily on precise timestamps.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

CPU spikes during leap second event  
scheduled jobs executing twice  
database replication lag  
authentication token validation failures  
unexpected cluster instability

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

appears like random infrastructure failure  
looks like NTP server issue  
seems like scheduler bug  
blamed on database contention  
appears as transient latency problem

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

kernel leap second handling bug  
outdated NTP configuration  
application assumes fixed 60-second minute  
timestamp parsing failure  
clock synchronization inconsistencies

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify NTP synchronization logs  
inspect system clock behavior  
review scheduler execution times  
check timestamp anomalies in logs  
confirm kernel and JVM time handling

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

system time drift metrics  
NTP daemon logs  
scheduler execution history  
database timestamp anomalies  
authentication token validation logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

tested leap second handling  
modern NTP configuration  
clock abstraction libraries  
kernel patch management  
time anomaly simulation

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>