# Pattern: Duplicate Event Processing

## Description

**Duplicate Event Processing** happens when the same event is consumed more than once and downstream systems process each copy as a new action.

This often creates invisible operational failures because infrastructure appears healthy while business outcomes become inconsistent.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

same email sent multiple times  
duplicate account updates  
inventory deducted twice  
multiple shipment creation  
unexpected reconciliation mismatches

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like user error  
appears like queue instability  
seems like database inconsistency  
blamed on upstream system  
appears as intermittent workflow bug

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

at-least-once delivery semantics  
consumer acknowledgment failures  
event replay after recovery  
missing deduplication logic  
consumer restart during processing

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review event IDs for duplicates  
inspect acknowledgment failures  
check consumer restart history  
validate deduplication controls  
compare processing timestamps

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

event processing logs  
message acknowledgment failures  
consumer restart events  
duplicate business action traces  
queue replay history

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

consumer deduplication  
idempotent event handlers  
safe acknowledgment patterns  
replay protection  
event uniqueness validation

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
