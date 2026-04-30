# Pattern: Dead Letter Queue Silent Explosion

## Description

**Dead Letter Queue Silent Explosion** happens when failed messages accumulate rapidly in a DLQ without triggering alerts, eventually overwhelming storage or hiding systemic failures.

This creates delayed outages and hidden data loss scenarios.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden spike in DLQ size  
processing delays in main queue  
missing downstream data  
storage usage unexpectedly high  
delayed failure discovery

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like slow consumer issue  
appears like storage growth anomaly  
blamed on traffic spike  
seems like queue backlog  
appears as minor retry issue

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missing DLQ monitoring  
high retry failure rate  
poison messages not handled  
consumer logic bugs  
lack of alert thresholds

---

# First Checks

Fast checks engineers should perform.

**Examples**:

inspect DLQ message volume  
review failure reasons in messages  
check consumer retry logic  
verify alerting configuration  
analyse message patterns

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

DLQ size metrics  
consumer failure logs  
retry attempt counts  
queue throughput metrics  
error message patterns

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

DLQ monitoring and alerting  
poison message handling strategy  
retry limits and backoff  
automated DLQ draining workflows  
failure visibility dashboards

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>