# Pattern: CPU Starvation

## Description

**CPU Starvation** occurs when critical processes do not receive enough CPU time to run efficiently because the available CPU capacity is fully consumed.

This pattern appears in production systems when compute-intensive workloads, runaway threads, noisy neighbours, or poor resource limits cause the CPU to remain saturated. As a result, request latency increases, queues grow, and time-sensitive operations begin to fail.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- High CPU usage
- Latency spike
- Request processing slowdown
- Queue depth growth
- Missed heartbeats or health checks
- Timeouts between services

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like application bug
- Appears like traffic spike
- Monitoring alerts from downstream service
- Seems like memory issue
- Appears like database slowdown

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- Unexpected traffic surge
- Inefficient code path
- Expensive background jobs
- Noisy neighbour workload
- Missing CPU limits or quotas
- Tight retry loops

---

## First Checks

Fast checks engineers should perform.

Examples:

- CPU utilisation by host or container
- Top processes or threads consuming CPU
- Request rate changes
- Background job activity
- Recent deployments
- Throttling or cgroup limits

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- CPU utilisation metrics
- container throttling metrics
- high-latency request traces
- thread-level CPU profiles
- system load averages
- scheduler delay metrics

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- autoscaling
- CPU profiling
- workload isolation
- resource limits
- performance testing
- rate limiting

---

<a href="../../categories/infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
