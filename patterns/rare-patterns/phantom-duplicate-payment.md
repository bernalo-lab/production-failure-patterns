# Pattern: Phantom Duplicate Payment Cascade

## Description

**Phantom Duplicate Payment Cascade** happens when payment systems unintentionally process the same transaction multiple times, often triggered by retries, race conditions, or replayed events.

This creates financial, legal, and trust issues at scale.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

customers charged multiple times  
duplicate transaction records  
refund requests spike  
payment reconciliation mismatch  
financial reporting inconsistencies

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like payment provider issue  
appears like user double submission  
blamed on frontend bug  
seems like database duplication  
appears as isolated transaction anomaly

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missing idempotency keys  
retry logic without safeguards  
race condition in payment processing  
event replay  
inconsistent transaction state handling

---

# First Checks

Fast checks engineers should perform.

**Examples**:

inspect transaction IDs  
verify idempotency controls  
review retry logs  
check payment provider responses  
analyse duplicate patterns

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

duplicate transaction logs  
payment reconciliation reports  
retry attempt metrics  
event processing history  
financial audit logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

strong idempotency enforcement  
safe retry design  
transaction deduplication  
payment workflow testing  
audit and reconciliation controls

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>