# Pattern: Ephemeral Storage Exhaustion

## Description

**Ephemeral Storage Exhaustion** happens when temporary local storage used by containers, pods, or virtual machines fills up and prevents applications from writing required runtime data.

This often impacts logs, temp files, caches, and intermediate processing, causing failures that appear unrelated to disk usage.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

containers restarting unexpectedly  
application write failures  
logs suddenly stop appearing  
temporary file creation errors  
pods evicted by orchestration platform

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like application crash  
appears like memory issue  
seems like logging system failure  
blamed on deployment instability  
appears as random container failure

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

log files growing without rotation  
temporary files not cleaned up  
large batch job output  
cache overflow  
container image layer growth

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review disk usage on affected nodes  
inspect temporary directory growth  
check log rotation behaviour  
validate container eviction events  
compare pod storage requests and limits

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

node disk usage metrics  
pod eviction events  
filesystem usage dashboards  
container restart logs  
log growth patterns

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

log rotation policies  
ephemeral storage limits  
cleanup jobs for temp files  
storage usage alerting  
container storage monitoring

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
