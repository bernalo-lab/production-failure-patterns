# Pattern: Retry Storm Triggered by Monitoring Failure

## Description

**Retry Storm Triggered by Monitoring Failure** happens when monitoring or alerting systems fail to detect an issue, allowing aggressive retry logic to escalate into a storm that overwhelms services.

This turns a small failure into a large-scale outage.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden traffic surge  
high error rates across services  
dependency saturation  
timeouts increasing rapidly  
cascading failures

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like traffic spike  
appears like DDoS attack  
blamed on user growth  
seems like scaling issue  
appears as random overload

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missing alert on initial failure  
aggressive retry configuration  
no circuit breaker  
monitoring blind spot  
delayed incident detection

---

# First Checks

Fast checks engineers should perform.

**Examples**:

inspect retry rates  
review monitoring alert history  
check dependency health  
verify circuit breaker status  
analyse traffic patterns

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

retry attempt logs  
traffic surge metrics  
dependency error rates  
alerting gaps  
request fan-out metrics

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

retry limits and backoff  
circuit breakers  
monitoring coverage audits  
early alerting thresholds  
chaos testing for retry behaviour

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>