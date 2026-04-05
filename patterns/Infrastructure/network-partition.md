# Pattern: Network Partition

## Description

A **Network Partition** occurs when one part of a distributed system loses communication with another part, even though the individual components may still be running.

This pattern appears in production systems when network paths break, routing changes fail, firewalls block traffic, or connectivity becomes unstable between nodes, services, or regions. The result is that different parts of the system begin operating with incomplete information, which can lead to timeouts, stale state, split-brain risks, and cascading failures.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- Timeouts between services
- Increased error rates on cross-service calls
- Replication failures between nodes
- Intermittent connectivity issues
- Sudden drop in successful requests between specific systems
- Cluster instability or leader election issues

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Appears like application crash
- Looks like service discovery issue
- Monitoring alerts from downstream service
- Seems like DNS problem
- Appears like partial regional outage

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- Firewall or security group misconfiguration
- Router or switch failure
- Broken network path between regions or zones
- Service mesh or proxy communication failure
- VPN or peering connection issue
- Packet loss or network congestion

---

## First Checks

Fast checks engineers should perform.

Examples:

- Connectivity between affected hosts
- Packet loss and latency metrics
- Network route changes
- Firewall and security group rules
- DNS resolution between nodes
- Cluster membership or leader status

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- connection timeout logs
- failed health checks
- packet loss metrics
- replication failure logs
- service-to-service latency metrics
- network path monitoring

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- multi-zone redundancy
- network path monitoring
- resilient retry policies
- quorum-based systems
- failover testing
- automated network configuration validation

---

<a href="../../categories/infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
