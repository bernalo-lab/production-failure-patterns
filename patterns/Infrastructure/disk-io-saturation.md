# Pattern: Disk IO Saturation

## Description

**Disk IO Saturation** occurs when the volume of read and write operations exceeds the available disk throughput or IOPS capacity.

This pattern appears in production systems when databases, logs, queues, or storage-heavy workloads generate more disk activity than the underlying storage can handle. As latency grows at the storage layer, applications begin to slow, requests pile up, and system-wide performance degrades.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- High disk wait times
- Slow database queries
- Increased request latency
- Queue depth growth
- Timeouts in storage-heavy services
- CPU waiting on IO despite moderate workload

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like database failure
- Appears like application slowdown
- Monitoring alerts from downstream service
- Seems like CPU problem
- Appears like general infrastructure instability

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- High write amplification
- Unoptimised queries or scans
- Log bursts under heavy load
- Storage device capacity limits
- Background compaction or indexing
- Multiple workloads sharing the same disk

---

## First Checks

Fast checks engineers should perform.

Examples:

- Disk utilisation and wait metrics
- Read and write throughput
- IO queue depth
- Slow query logs
- Storage class or volume performance limits
- Recent workload spikes

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- disk wait metrics
- IO queue depth metrics
- slow query logs
- storage latency graphs
- filesystem saturation alerts
- service latency correlated with IO spikes

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- faster storage tiers
- workload isolation
- query optimisation
- caching
- disk performance monitoring
- capacity planning

---

<a href="../../categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
