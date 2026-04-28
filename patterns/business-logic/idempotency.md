# Pattern: Idempotency Failure

## Description

**Idempotency Failure** happens when the same operation is processed multiple times and produces different or duplicate outcomes instead of safely returning the same result.

This creates financial errors, duplicate records, repeated notifications, and inconsistent workflow behaviour, especially in distributed systems with retries and async processing.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

duplicate payments created  
multiple orders for one request  
repeated customer notifications  
unexpected inventory reduction  
inconsistent transaction history

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like user submitted twice  
appears like frontend bug  
seems like payment gateway issue  
blamed on retry infrastructure  
appears as random business error

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missing idempotency keys  
retry logic without deduplication  
race conditions during writes  
partial transaction commits  
event replay without safeguards

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify duplicate request identifiers  
check retry history  
inspect transaction boundaries  
review event replay logs  
compare request timestamps

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

duplicate transaction logs  
request correlation IDs  
retry event history  
payment processing traces  
database write timestamps

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

idempotency keys  
deduplication layers  
safe retry design  
transaction boundary validation  
event replay controls

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
