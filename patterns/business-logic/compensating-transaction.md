# Pattern: Compensating Transaction Failure

## Description

**Compensating Transaction Failure** happens when rollback or recovery actions meant to reverse a failed workflow also fail, leaving the system in a partially completed and inconsistent state.

This is especially dangerous in payment systems, booking flows, and distributed transaction processes.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

payment captured but order cancelled  
refund fails after transaction rollback  
inventory reserved but never released  
user charged without service delivery  
partial workflow completion across systems

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like payment provider issue  
appears like order processing bug  
seems like user workflow problem  
blamed on integration instability  
appears as isolated transaction error

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

rollback logic not tested  
compensation step dependency failure  
missing retry safeguards  
manual intervention during rollback  
partial external system completion

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review transaction step history  
verify compensation execution status  
inspect external provider responses  
check partial completion boundaries  
validate rollback retry attempts

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

workflow transaction logs  
rollback execution events  
payment provider callbacks  
inventory reservation history  
compensation failure traces

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

tested compensation workflows  
explicit rollback observability  
safe retry controls  
transaction state auditing  
failure simulation for rollback paths

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>