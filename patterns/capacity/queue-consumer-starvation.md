# Pattern: Queue Consumer Starvation

## Description

**Queue Consumer Starvation** happens when message producers continue publishing work, but consumers cannot process messages fast enough to keep up.

This creates backlog growth, delayed processing, and eventually downstream failures as dependent workflows stall.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

queue depth increasing rapidly  
processing delays growing  
timeouts in downstream workflows  
retry storms from delayed events  
consumer lag alerts firing

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like producer overload  
appears like network issue  
seems like broker instability  
blamed on dependency failures  
appears as application slowness

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

consumer crashes  
slow message handlers  
insufficient worker scaling  
poison messages blocking progress  
dependency slowness downstream

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review consumer lag  
inspect worker health  
check poison message patterns  
validate dependency latency  
compare producer vs consumer rates

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

queue depth metrics  
consumer lag dashboards  
worker crash logs  
message retry traces  
dependency latency metrics

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

consumer autoscaling  
dead-letter queues  
poison message isolation  
queue backlog alerting  
throughput load testing

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
