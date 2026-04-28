# Pattern: Zombie Process / Orphaned Workflow

## Description

**Zombie Process / Orphaned Workflow** happens when background jobs, transactions, or workflows continue running without ownership, visibility, or proper completion paths.

These hidden processes consume resources, create stale state, and silently block normal operations.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

long-running stuck background jobs  
orders permanently in processing state  
resources reserved but never released  
unexpected capacity consumption  
manual cleanup repeatedly required

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like workflow delay  
appears like queue backlog  
seems like database lock issue  
blamed on slow dependency recovery  
appears as random operational noise

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missing timeout boundaries  
worker crash during execution  
orchestrator losing state ownership  
failed cleanup handlers  
incomplete failure recovery paths

---

# First Checks

Fast checks engineers should perform.

**Examples**:

identify long-running stale workflows  
inspect worker crash history  
validate timeout and cleanup rules  
review ownership tracking  
compare expected versus active process counts

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

workflow execution age metrics  
worker failure logs  
orphaned resource dashboards  
cleanup failure events  
stale transaction monitoring

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

explicit workflow timeouts  
ownership tracking validation  
automated stale process cleanup  
recovery path testing  
orphan detection alerts

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;"><<Back</a>