# Pattern: Node Resource Starvation

## Description

Node Resource Starvation occurs when a host or Kubernetes node runs out of critical shared resources such as CPU, memory, disk, or network capacity, causing workloads on that node to degrade.

This pattern frequently causes multiple unrelated services to fail simultaneously because they share the same infrastructure dependency.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Multiple services slowing down
Pod evictions
Increased latency across workloads
Node instability
Failed scheduling

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like application-wide failure
Appears like dependency outage
Seems like database issue
Monitoring shows service failures everywhere

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

Noisy neighbour workloads
Missing resource quotas
Overcommitted nodes
Unexpected traffic spikes
Disk saturation
Memory pressure

---

# First Checks

Fast checks engineers should perform.

**Examples**:

Node CPU and memory metrics
Disk I/O and disk space
Pod resource requests and limits
Recent deployments
Eviction events
Scheduling failures

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

node resource metrics
pod eviction logs
scheduler events
disk pressure alerts
system load averages

---

# Prevention

What can reduce the likelihood of this pattern.

Examples:

node autoscaling
resource quotas
workload isolation
proper requests and limits
capacity planning

---

<a href="../../categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>