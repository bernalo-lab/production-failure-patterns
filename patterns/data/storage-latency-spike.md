# Pattern: Storage Latency Spike

## Description

A Storage Latency Spike occurs when the time required to read or write data from persistent storage suddenly increases.

This pattern often appears in distributed systems when storage nodes become overloaded, disks enter degraded states, or background maintenance tasks interfere with normal workloads. Even small increases in storage latency can cascade into application-level timeouts and system instability.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Sudden increase in read/write latency
Application requests timing out
Database queries slowing down
Queue processing delays
Increased I/O wait times

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Appears like CPU bottleneck
Looks like database query inefficiency
Appears as application performance issue
Monitoring suggests network slowdown

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

overloaded storage nodes
degraded disk performance
background compaction jobs
snapshot operations
storage throttling by cloud provider
burst I/O limits being exceeded

---

# First Checks

Fast checks engineers should perform.

**Examples**:

storage read/write latency metrics
disk I/O utilisation
I/O wait metrics on database hosts
background storage tasks
recent infrastructure changes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

disk latency metrics
storage throughput graphs
I/O wait metrics
database disk usage logs
cloud storage performance metrics

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

capacity planning for storage
monitoring disk latency thresholds
separating workloads across volumes
autoscaling storage clusters
proactive disk health monitoring

---

<a href="../../categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
