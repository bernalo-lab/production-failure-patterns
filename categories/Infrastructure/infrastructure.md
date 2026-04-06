# Category: Infrastructure Failure Patterns

---

# 01. Pattern: CPU Starvation

## Description
<a href="../patterns/infrastructure/cpu-starvation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**CPU Starvation**</a> occurs when critical processes do not receive enough CPU time to run efficiently because the available CPU capacity is fully consumed.

This pattern appears in production systems when compute-intensive workloads, runaway threads, noisy neighbours, or poor resource limits cause the CPU to remain saturated. As a result, request latency increases, queues grow, and time-sensitive operations begin to fail.

---

# 02. Pattern: Disk IO Saturation

## Description
<a href="../../patterns/infrastructure/disk-io-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Disk IO Saturation**</a> occurs when the volume of read and write operations exceeds the available disk throughput or IOPS capacity.

This pattern appears in production systems when databases, logs, queues, or storage-heavy workloads generate more disk activity than the underlying storage can handle. As latency grows at the storage layer, applications begin to slow, requests pile up, and system-wide performance degrades.

---

# 03. Pattern: DNS Resolution Failure

## Description
A <a href="../../patterns/infrastructure/dns-resolution-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**DNS Resolution Failure**</a> occurs when services or clients cannot correctly resolve hostnames into IP addresses.

This pattern appears in production systems when DNS servers fail, records expire unexpectedly, service discovery breaks, or clients cache stale records. Since many services depend on DNS for locating internal and external dependencies, even a small DNS issue can cause widespread communication failures across the system.

---

# 04. Pattern: load-balancer-saturation

## Description
<a href="../../patterns/infrastructure/load-balancer-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Load Balancer Saturation**</a> occurs when a load balancer becomes a bottleneck and can no longer efficiently distribute incoming traffic.

This pattern appears in production systems when traffic exceeds capacity, connection limits are reached, health checks become unstable, or the load balancer itself runs out of resources. Even when backend services are healthy, a saturated load balancer can create system-wide latency, dropped requests, and uneven traffic distribution.

---

# 05. Pattern: network-partition

## Description
A <a href="../../patterns/infrastructure/load-balancer-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Network Partition**</a> occurs when one part of a distributed system loses communication with another part, even though the individual components may still be running.

This pattern appears in production systems when network paths break, routing changes fail, firewalls block traffic, or connectivity becomes unstable between nodes, services, or regions. The result is that different parts of the system begin operating with incomplete information, which can lead to timeouts, stale state, split-brain risks, and cascading failures.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
