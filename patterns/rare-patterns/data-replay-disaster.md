# Pattern: Data Replay Disaster

## Description

**Data Replay Disaster** happens when old messages, events, or transactions are unintentionally replayed into production systems, causing duplicate actions, financial errors, or widespread state corruption.

This is especially dangerous in payment systems, event-driven platforms, and distributed workflows where replayed operations are not safely idempotent.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

duplicate payments processed  
orders recreated unexpectedly  
inventory deducted multiple times  
historical events reappearing in queues  
customer notifications sent repeatedly

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like duplicate event producer issue  
appears like payment provider fault  
blamed on queue instability  
seems like database corruption  
appears as random workflow duplication

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

manual queue replay mistake  
offset reset during consumer recovery  
backup restore reintroduced old events  
idempotency protection missing  
reprocessing script executed incorrectly

---

# First Checks

Fast checks engineers should perform.

**Examples**:

inspect message timestamps  
verify queue consumer offsets  
review replay and restore activity  
check idempotency protection status  
confirm duplicate transaction boundaries

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

consumer offset history  
queue replay audit logs  
duplicate transaction records  
payment reconciliation reports  
workflow event history

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

strong idempotency controls  
replay-safe architecture  
protected queue replay operations  
explicit audit trails  
tested disaster recovery procedures

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>