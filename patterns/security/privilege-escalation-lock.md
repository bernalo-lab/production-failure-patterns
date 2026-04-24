# Pattern: Privilege Escalation Lockout

## Description

**Privilege Escalation Lockout** occurs when administrative access paths fail due to broken elevation controls, expired emergency access, or incorrect privilege boundaries.

This can prevent responders from accessing critical systems during incidents, increasing outage duration and operational risk.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Admin access denied  
Emergency access unavailable  
Deployment rollback blocked  
Incident response delayed  
Operational tasks cannot complete

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like IAM outage  
Appears like MFA problem  
Seems like identity provider failure  
Monitoring shows authentication issues only

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

broken sudo policies  
expired break-glass accounts  
incorrect privilege boundaries  
role assumption failures  
misconfigured admin groups

---

# First Checks

Fast checks engineers should perform.

**Examples**:

break-glass account status  
recent privilege changes  
admin role assignments  
MFA enforcement changes  
identity provider logs

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

access denied logs  
admin role audit trails  
privilege escalation failures  
MFA rejection logs  
identity provider events

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

tested break-glass access  
regular privilege audits  
emergency access validation  
separation of duties reviews  
automated escalation checks

---

<a href="../../categories/security/security.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>