# Pattern: Retry Without State Validation

## Description

**Retry Without State Validation** happens when failed operations are retried without first checking whether the previous attempt partially or fully succeeded.

This creates duplicate actions, financial inconsistencies, and hidden business workflow corruption.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

duplicate refunds issued  
multiple shipment creation  
inventory deducted twice  
repeated account provisioning  
workflow completion with inconsistent records

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like retry system working correctly  
appears like user repeated request  
seems like payment duplication bug  
blamed on event replay  
appears as isolated transaction issue

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missing state validation before retry  
timeout ambiguity from downstream service  
partial commit before failure response  
stateless retry design  
lack of reconciliation checks

---

# First Checks

Fast checks engineers should perform.

**Examples**:

inspect prior execution state  
review downstream success confirmation  
compare retry timestamps  
validate transaction completion markers  
check duplicate action history

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

retry execution logs  
transaction completion records  
duplicate workflow events  
payment confirmation traces  
state reconciliation reports

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

state validation before retry  
idempotent retry patterns  
transaction completion markers  
safe timeout handling  
workflow reconciliation checks

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
