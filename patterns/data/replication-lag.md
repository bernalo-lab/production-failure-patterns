# Pattern: Replication Lag

## Description

**Replication Lag** occurs when a replica database or storage node falls behind the primary and no longer reflects current data in real time.

This pattern appears in production systems when write volume increases, replication channels slow down, network connectivity degrades, or replicas lack sufficient resources to keep up. As the lag grows, applications reading from replicas may serve stale data, causing inconsistent user behaviour and hard-to-diagnose incidents.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- Stale reads
- Data inconsistencies between systems
- Increased lag metrics on replicas
- Delayed analytics or reporting jobs
- Requests behaving differently depending on read path
- Replication queue growth

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like application bug
- Appears like cache inconsistency
- Monitoring alerts from downstream service
- Seems like user session issue
- Appears like write failure

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- High write throughput on primary
- Slow replica storage performance
- Network latency between primary and replica
- Long-running queries on replica
- Resource constraints on follower nodes
- Replication process failure or backlog

---

## First Checks

Fast checks engineers should perform.

Examples:

- Current replication lag metrics
- Write volume on primary
- Replica CPU, memory, and IO usage
- Long-running queries on replica
- Replication error logs
- Network latency between nodes

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- replication lag metrics
- replica apply delay logs
- write throughput metrics
- replication backlog size
- stale read error reports
- primary-to-replica latency metrics

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- replica monitoring
- read routing controls
- faster replica storage
- workload isolation
- replication capacity planning
- query optimisation on replicas

---

<a href="../../categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
