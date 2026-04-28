# Pattern: Payment State Inconsistency

## Description

**Payment State Inconsistency** happens when payment status differs across systems such as payment gateways, internal ledgers, order systems, and customer records.

The payment may be successful in one system and failed or pending in another, creating operational confusion and customer trust issues.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

customer charged but order shows unpaid  
refund completed but account still shows pending  
payment marked failed but funds captured  
reconciliation mismatches during finance review  
manual support tickets increasing rapidly

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like gateway outage  
appears like frontend payment issue  
seems like accounting reconciliation bug  
blamed on customer payment method  
appears as isolated payment failure

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missed payment callback events  
partial transaction commits  
async event delivery delays  
retry without reconciliation checks  
external provider timeout ambiguity

---

# First Checks

Fast checks engineers should perform.

**Examples**:

compare payment gateway status with internal records  
review callback delivery logs  
inspect transaction timestamps  
validate retry and reconciliation history  
check failed webhook deliveries

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

payment gateway callbacks  
ledger transaction logs  
webhook failure events  
reconciliation reports  
customer support incident patterns

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

payment reconciliation jobs  
webhook retry safety  
transaction state auditing  
idempotent payment updates  
provider callback monitoring

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
