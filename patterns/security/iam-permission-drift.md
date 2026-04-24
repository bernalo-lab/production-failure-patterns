# Pattern: IAM Permission Drift

## Description

**IAM Permission Drift** occurs when access permissions gradually diverge from intended policy due to manual changes, inconsistent deployments, or unmanaged exceptions.

This creates production outages when services suddenly lose required access or gain unintended permissions that trigger security controls.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Access denied errors  
Unexpected 403 responses  
Deployment failures  
Broken service integrations  
Scheduled jobs suddenly failing

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like application bug  
Appears like secret failure  
Seems like dependency outage  
Monitoring points to downstream system

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

manual policy changes  
role inheritance issues  
stale infrastructure-as-code  
environment drift  
incorrect least privilege enforcement

---

# First Checks

Fast checks engineers should perform.

**Examples**:

recent IAM policy changes  
role attachment history  
audit trail events  
deployment differences  
access simulation tests

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

authorization failure logs  
cloud audit logs  
policy diff history  
403 metrics  
role assumption failures

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

policy-as-code  
permission drift detection  
automated access reviews  
least privilege testing  
change approval workflows

---

<a href="../../categories/security/security.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>