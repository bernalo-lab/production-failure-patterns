# Pattern: Firewall Rule Drift

## Description

**Firewall Rule Drift** occurs when firewall policies gradually diverge from intended design due to manual changes, temporary exceptions, or inconsistent deployments.

This can silently introduce outages by blocking legitimate traffic or create security risks by leaving unintended access paths open.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Unexpected blocked traffic  
Service communication failures  
Deployment rollbacks failing  
Intermittent access issues  
Production-only connectivity problems

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like network instability  
Appears like dependency outage  
Seems like application regression  
Monitoring points to downstream systems

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

manual firewall updates  
temporary emergency exceptions  
policy inconsistency across environments  
stale change documentation  
missing configuration sync

---

# First Checks

Fast checks engineers should perform.

**Examples**:

recent firewall policy changes  
rule comparison across environments  
blocked ports and protocols  
traffic path validation  
change approval history

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

firewall deny logs  
network flow monitoring  
policy diff history  
connection failure logs  
audit trail events

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

policy-as-code  
regular firewall audits  
drift detection automation  
temporary rule expiration controls  
environment consistency checks

---

<a href="../../categories/security/security.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>