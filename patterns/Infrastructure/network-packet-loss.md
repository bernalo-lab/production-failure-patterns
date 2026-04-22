# Pattern: Network Packet Loss

## Description

Network Packet Loss occurs when packets fail to reach their destination across the network, causing retransmissions, latency spikes, and intermittent failures.

This pattern often creates confusing production incidents because applications appear partially healthy while requests randomly fail.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Intermittent request failures
Increased latency
Connection timeouts
Retries increasing
Service-to-service instability

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like application bug
Appears like dependency outage
Seems like DNS issue
Monitoring shows partial service health

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

overloaded network interface
faulty hardware
cloud network degradation
misconfigured load balancer
packet drops from firewall rules
MTU mismatch

---

# First Checks

Fast checks engineers should perform.

**Examples**:

packet loss metrics
network interface health
retransmission rates
dependency connectivity checks
recent network changes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

packet retransmission metrics
TCP timeout logs
network interface errors
dependency latency graphs
connection reset logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

network health monitoring
redundancy
proper MTU configuration
capacity planning
load balancer testing

---

<a href="../../categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>