# Pattern: Terraform State Corruption

## Description

**Terraform State Corruption** occurs when the Terraform state file becomes inconsistent, incomplete, locked incorrectly, or no longer reflects the real infrastructure.

This makes deployments dangerous because Terraform may destroy, recreate, or lose track of critical production resources.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

unexpected resource recreation plans  
state lock errors  
missing tracked resources  
failed apply operations  
dangerous drift during deployment

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like provider API issue  
Appears like infrastructure outage  
Seems like deployment bug  
Monitoring shows resources healthy

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

manual state file edits  
interrupted terraform apply  
backend storage corruption  
concurrent apply conflicts  
improper state migration

---

# First Checks

Fast checks engineers should perform.

**Examples**:

terraform state validation  
backend lock inspection  
resource state comparison  
recent apply history  
manual state modifications

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

terraform plan output  
state backend logs  
lock failure messages  
resource drift reports  
apply execution history

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

remote state backends  
state locking enforcement  
restricted manual state access  
regular backup of state files  
controlled infrastructure workflows

---

<a href="../../categories/deployment/deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>