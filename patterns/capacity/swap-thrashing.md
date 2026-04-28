# Pattern: Swap Thrashing

## Description

**Swap Thrashing** happens when the operating system spends excessive time moving memory pages between RAM and disk swap instead of executing useful work.

This creates severe performance degradation because disk-based memory access is far slower than physical memory access.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

extreme latency spikes  
high disk usage with low throughput  
CPU appears busy but work slows down  
application response times become unpredictable  
node performance collapses gradually

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like CPU bottleneck  
appears like disk IOPS issue  
seems like dependency latency  
blamed on traffic spikes  
appears as random node instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

memory pressure exceeding RAM  
misconfigured JVM heap sizes  
container memory limits too high  
memory leaks  
oversubscribed virtual machines

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review swap usage metrics  
inspect memory consumption trends  
check page fault rates  
validate container memory limits  
compare RAM usage against workload patterns

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

swap usage dashboards  
major page fault metrics  
memory pressure alerts  
node performance graphs  
OOM warning logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

proper memory sizing  
swap monitoring alerts  
memory leak detection  
safe container memory limits  
heap tuning and validation

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
