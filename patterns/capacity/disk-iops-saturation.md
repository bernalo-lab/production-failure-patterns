# Pattern: Disk IOPS Saturation

## Description

**Disk IOPS Saturation** happens when storage systems reach their input/output operation limits, causing read and write operations to slow dramatically.

Applications may appear healthy at first, but latency grows quickly as requests wait for blocked storage operations.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

database latency spikes  
slow application response times  
write operations timing out  
high disk wait times  
queue depth growth on storage volumes

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like database bug  
appears like network latency  
seems like CPU bottleneck  
blamed on bad deployment  
appears as dependency slowdown

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

unexpected write amplification  
backup jobs competing for IOPS  
index rebuild operations  
high retry write storms  
storage class under-provisioning

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review disk IOPS metrics  
check disk queue depth  
inspect backup or batch jobs  
validate database write volume  
compare provisioned vs consumed IOPS

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

disk latency dashboards  
IOPS usage metrics  
storage queue depth  
database write wait events  
backup job execution logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

storage capacity planning  
IOPS monitoring  
workload isolation  
scheduled heavy batch operations  
storage performance testing

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>