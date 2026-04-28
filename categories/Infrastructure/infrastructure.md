# Category: Infrastructure Failure Patterns

## Description
These failures originate from the platform layer including compute, containers, nodes, networking, and operating systems. They are especially common in Kubernetes, cloud environments, and large-scale distributed systems.

---

# 01. Pattern: CPU Starvation

## Description
<a href="../../patterns/Infrastructure/cpu-starvation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**CPU Starvation**</a> occurs when critical processes do not receive enough CPU time to run efficiently because the available CPU capacity is fully consumed.

This pattern appears in production systems when compute-intensive workloads, runaway threads, noisy neighbours, or poor resource limits cause the CPU to remain saturated. As a result, request latency increases, queues grow, and time-sensitive operations begin to fail.

---

# 02. Pattern: Disk IO Saturation

## Description
<a href="../../patterns/Infrastructure/disk-io-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Disk IO Saturation**</a> occurs when the volume of read and write operations exceeds the available disk throughput or IOPS capacity.

This pattern appears in production systems when databases, logs, queues, or storage-heavy workloads generate more disk activity than the underlying storage can handle. As latency grows at the storage layer, applications begin to slow, requests pile up, and system-wide performance degrades.

---

# 03. Pattern: DNS Resolution Failure

## Description
A <a href="../../patterns/Infrastructure/dns-resolution-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**DNS Resolution Failure**</a> occurs when services or clients cannot correctly resolve hostnames into IP addresses.

This pattern appears in production systems when DNS servers fail, records expire unexpectedly, service discovery breaks, or clients cache stale records. Since many services depend on DNS for locating internal and external dependencies, even a small DNS issue can cause widespread communication failures across the system.

---

# 04. Pattern: Load Balancer Saturation

## Description
<a href="../../patterns/Infrastructure/load-balancer-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Load Balancer Saturation**</a> occurs when a load balancer becomes a bottleneck and can no longer efficiently distribute incoming traffic.

This pattern appears in production systems when traffic exceeds capacity, connection limits are reached, health checks become unstable, or the load balancer itself runs out of resources. Even when backend services are healthy, a saturated load balancer can create system-wide latency, dropped requests, and uneven traffic distribution.

---

# 05. Pattern: Network Partition

## Description
A <a href="../../patterns/Infrastructure/load-balancer-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Network Partition**</a> occurs when one part of a distributed system loses communication with another part, even though the individual components may still be running.

This pattern appears in production systems when network paths break, routing changes fail, firewalls block traffic, or connectivity becomes unstable between nodes, services, or regions. The result is that different parts of the system begin operating with incomplete information, which can lead to timeouts, stale state, split-brain risks, and cascading failures.

---

# 06. Pattern: Memory Exhaustion

## Description
<a href="../../patterns/Infrastructure/memory-exhaustion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Memory Exhaustion**</a> occurs when a system or service consumes all available memory, leading to degraded performance, crashes, or forced process termination.

This pattern commonly appears in production systems due to memory leaks, unbounded caching, or sudden spikes in workload. In containerised environments, it often triggers OOM (Out Of Memory) kills, restarting services and disrupting availability.

---

# 07. Pattern: Container Restart Loop

## Description
<a href="../../patterns/Infrastructure/container-restart-loop.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Container Restart Loop**</a> occurs when a container repeatedly crashes and is automatically restarted by the orchestration system (e.g., Kubernetes CrashLoopBackOff).

This pattern appears when applications fail during startup or shortly after, causing continuous restarts that prevent the service from stabilising.

---

# 08. Pattern: Node Resource Starvation

## Description
<a href="../../patterns/Infrastructure/node-resource-starvation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Node Resource Starvation**</a> occurs when a host or Kubernetes node runs out of critical shared resources such as CPU, memory, disk, or network capacity, causing workloads on that node to degrade.

This pattern frequently causes multiple unrelated services to fail simultaneously because they share the same infrastructure dependency.

---

# 09. Pattern: Auto-Scaling Failure

## Description
An <a href="../../patterns/Infrastructure/auto-scaling-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Auto-Scaling Failure**</a> occurs when systems fail to scale up or down appropriately in response to changing demand.

This creates either under-provisioning (causing incidents) or over-provisioning (causing unnecessary cost). In production, under-scaling is usually the dangerous failure mode.

---

# 10. Pattern: Network Packet Loss

## Description
<a href="../../patterns/Infrastructure/network-packet-loss.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Network Packet Loss**</a> occurs when packets fail to reach their destination across the network, causing retransmissions, latency spikes, and intermittent failures.

This pattern often creates confusing production incidents because applications appear partially healthy while requests randomly fail.

---

# 11. Pattern: Port Exhaustion

## Description
<a href="../../patterns/Infrastructure/port-exhaustion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Port Exhaustion**</a> occurs when a system runs out of available ephemeral ports required for outbound connections.

This commonly affects high-throughput systems making large numbers of short-lived network calls and can cause sudden widespread connection failures.

---

# 12. Pattern: Kernel Resource Limits Reached

## Description
<a href="../../patterns/Infrastructure/kernel-resource-limits.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Kernel Resource Limits Reached**</a> occurs when operating system-level limits such as file descriptors, process limits, sockets, or threads are exhausted.

This creates sudden failures even when application metrics appear healthy because the failure occurs below the application layer.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<< Back**</a>
