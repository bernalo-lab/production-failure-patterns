# Pattern: Port Exhaustion

## Description

Port Exhaustion occurs when a system runs out of available ephemeral ports required for outbound connections.

This commonly affects high-throughput systems making large numbers of short-lived network calls and can cause sudden widespread connection failures.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Connection failures
Increased timeout rates
Retry storms
Downstream service errors
Intermittent dependency failures

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like dependency outage
Appears like DNS problem
Seems like firewall issue
Monitoring suggests downstream instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

excessive short-lived connections
missing connection pooling
aggressive retries
slow TIME_WAIT cleanup
high outbound request volume

---

# First Checks

Fast checks engineers should perform.

**Examples**:

open socket count
ephemeral port usage
TIME_WAIT state count
retry behaviour
connection pool settings

---

#Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

socket state metrics
connection refused logs
retry metrics
network port utilisation
TIME_WAIT statistics

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

connection pooling
retry budgets
keep-alive optimisation
ephemeral port tuning
reduced unnecessary outbound calls

---

<a href="../../categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>