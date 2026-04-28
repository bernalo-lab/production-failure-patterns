# Pattern: Scheduled Job Overlap Collision

## Description

**Scheduled Job Overlap Collision** happens when recurring jobs start before previous executions have completed, causing duplicate work, contention, or conflicting updates.

This is common in reporting jobs, billing runs, cleanup tasks, and data synchronisation processes.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

duplicate billing runs  
database contention during batch jobs  
unexpected lock contention  
reports generated multiple times  
system slowdown during scheduled windows

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like database issue  
appears like scheduler instability  
seems like queue congestion  
blamed on infrastructure slowdown  
appears as random overnight failures

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

job duration exceeding schedule interval  
missing execution locks  
retry starting overlapping runs  
manual reruns during active execution  
scheduler misconfiguration

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review job execution history  
compare job duration versus schedule interval  
validate execution lock controls  
inspect retry-triggered reruns  
check scheduler configuration changes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

scheduler execution logs  
job overlap timestamps  
database lock contention metrics  
batch process dashboards  
manual rerun audit logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

job execution locking  
schedule interval validation  
overlap detection alerts  
safe manual rerun controls  
runtime monitoring for scheduled jobs

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
