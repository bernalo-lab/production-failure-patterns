# Pattern: Noisy Neighbour Resource Contention

## Description

**Noisy Neighbour Resource Contention** happens when one workload consumes disproportionate shared resources such as CPU, memory, disk, or network bandwidth, degrading the performance of nearby workloads.

This is common in shared infrastructure such as Kubernetes nodes, VMs, and multi-tenant cloud environments.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

one service slows while others spike resource usage  
random latency on healthy applications  
CPU throttling without obvious local cause  
disk latency spikes from unrelated workloads  
performance degradation on shared nodes

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like application inefficiency  
appears like database slowness  
seems like cloud provider issue  
blamed on traffic imbalance  
appears as isolated service instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missing resource limits  
batch jobs consuming shared capacity  
poor workload scheduling  
overcommitted nodes  
unexpected background processes

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review node-level resource usage  
identify top resource-consuming workloads  
check container resource limits  
inspect scheduling decisions  
compare affected and unaffected nodes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

node CPU and memory metrics  
container throttling events  
disk and network usage dashboards  
scheduler placement logs  
resource contention alerts

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

resource requests and limits  
workload isolation policies  
node affinity rules  
tenant-aware scheduling  
capacity reservation for critical services

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
