# Pattern: Infrastructure Drift After Deploy

## Description

**Infrastructure Drift After Deploy** occurs when the live production environment no longer matches the intended declared infrastructure state after deployment.

This creates hidden instability because systems behave differently from what deployment automation expects.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

unexpected production failures  
manual fixes stop working  
configuration mismatches  
deployment inconsistencies  
environment-specific incidents

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like application regression  
Appears like cloud provider issue  
Seems like deployment tool bug  
Monitoring shows healthy resources

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

manual production changes  
failed infrastructure sync  
out-of-band hotfixes  
partial IaC application  
configuration drift over time

---

# First Checks

Fast checks engineers should perform.

**Examples**:

infrastructure state comparison  
recent manual production changes  
drift detection reports  
resource configuration differences  
deployment history

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

IaC drift reports  
resource audit logs  
configuration mismatch alerts  
deployment change history  
manual admin action logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

strict infrastructure as code  
drift detection automation  
restricted manual production changes  
regular reconciliation jobs  
deployment compliance checks

---

<a href="../../categories/deployment/deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>