# Pattern: Poison Message Loop

## Description

**Poison Message Loop** happens when a malformed or problematic message repeatedly fails processing and is continuously retried without resolution.

This blocks consumer throughput, increases queue pressure, and creates hidden operational failures that appear as platform instability.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

same message failing repeatedly  
queue depth growing continuously  
consumer throughput drops sharply  
retry storms on one workflow  
delayed processing for healthy messages

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like broker outage  
appears like consumer crash  
seems like dependency failure  
blamed on infrastructure instability  
appears as random queue slowdown

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

invalid payload format  
unexpected schema changes  
missing downstream dependency  
unhandled edge case logic  
no dead-letter queue configuration

---

# First Checks

Fast checks engineers should perform.

**Examples**:

identify repeatedly failing message IDs  
inspect payload structure  
review consumer exception logs  
check dead-letter queue status  
validate schema compatibility

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

consumer failure logs  
retry count metrics  
dead-letter queue events  
message processing traces  
queue backlog dashboards

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

dead-letter queues  
retry limits  
schema validation before enqueue  
poison message isolation  
consumer exception alerting

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
