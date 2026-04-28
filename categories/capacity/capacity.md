# Category: Capacity & Performance Failure Patterns

## Description
These failures develop when systems gradually or suddenly exceed resource limits such as CPU, memory, disk, queues, or scaling boundaries. They often begin as slow degradation before escalating into full production incidents.

---

# 01. Pattern: Slow Burn Capacity Exhaustion

## Description

<a href="../../patterns/capacity/slow-burn-capacity-exhaustion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Slow Burn Capacity Exhaustion**</a> happens when system resources gradually degrade over time rather than failing suddenly.

Unlike sharp incidents, this pattern slowly builds through increasing load, inefficient usage, or hidden leaks until latency rises, retries increase, and the platform eventually reaches failure thresholds.

---

# 02. Pattern: Burst Traffic Saturation

## Description

<a href="../../patterns/capacity/burst-traffic-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Burst Traffic Saturation**</a> happens when sudden spikes in traffic exceed system capacity faster than scaling or protection mechanisms can respond.

This creates rapid latency increases, request failures, and cascading retries that can overwhelm otherwise healthy services.

---

# 03. Pattern: Connection Leak Saturation

## Description

<a href="../../patterns/capacity/connection-leak-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Connection Leak Saturation**</a> happens when database, API, or service connections are opened but not properly released, gradually exhausting available connection capacity.

This causes request failures even though the downstream dependency itself may still be healthy.

---

# 04. Pattern: Queue Consumer Starvation

## Description

<a href="../../patterns/capacity/queue-consumer-starvation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Queue Consumer Starvation**</a> happens when message producers continue publishing work, but consumers cannot process messages fast enough to keep up.

This creates backlog growth, delayed processing, and eventually downstream failures as dependent workflows stall.

---

# 05. Pattern: Disk IOPS Saturation

## Description

<a href="../../patterns/capacity/disk-iops-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Disk IOPS Saturation**</a> happens when storage systems reach their input/output operation limits, causing read and write operations to slow dramatically.

Applications may appear healthy at first, but latency grows quickly as requests wait for blocked storage operations.

---

# 06. Pattern: Ephemeral Storage Exhaustion

## Description

<a href="../../patterns/capacity/ephemeral-storage-exhaustion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Ephemeral Storage Exhaustion**</a> happens when temporary local storage used by containers, pods, or virtual machines fills up and prevents applications from writing required runtime data.

This often impacts logs, temp files, caches, and intermediate processing, causing failures that appear unrelated to disk usage.

---

# 07. Pattern: Swap Thrashing

## Description

<a href="../../patterns/capacity/swap-thrashing.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Swap Thrashing**</a> happens when the operating system spends excessive time moving memory pages between RAM and disk swap instead of executing useful work.

This creates severe performance degradation because disk-based memory access is far slower than physical memory access.

---

# 08. Pattern: Noisy Neighbour Resource Contention

## Description

<a href="../../patterns/capacity/noisy-neighbour-resource.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Noisy Neighbour Resource Contention**</a> happens when one workload consumes disproportionate shared resources such as CPU, memory, disk, or network bandwidth, degrading the performance of nearby workloads.

This is common in shared infrastructure such as Kubernetes nodes, VMs, and multi-tenant cloud environments.

---

# 09. Pattern: Autoscaler Feedback Loop Failure

## Description

<a href="../../patterns/capacity/autoscaler-feedback-loop.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Autoscaler Feedback Loop Failure**</a> happens when scaling systems respond too slowly, too aggressively, or based on misleading signals, causing instability instead of recovery.

Instead of stabilising the platform, scaling actions amplify the incident through oscillation, delayed recovery, or resource waste.

---

# 10. Pattern: Cold Start Amplification

## Description

<a href="../../patterns/capacity/cold-start-amplification.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Cold Start Amplification**</a> happens when new instances, containers, or serverless functions take too long to become useful during traffic spikes or recovery events.

Instead of relieving pressure, startup delays increase retries, queue growth, and cascading failures across the platform.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
