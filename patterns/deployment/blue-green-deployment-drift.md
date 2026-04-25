# Pattern: Blue-Green Deployment Drift

## Description

**Blue-Green Deployment Drift** occurs when the blue and green environments gradually stop matching each other due to configuration differences, data mismatches, or infrastructure changes.

When traffic switches, unexpected failures occur because the standby environment is no longer truly production-ready.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Unexpected failures after environment switch  
Configuration mismatch errors  
Missing dependencies in target environment  
Authentication failures after cutover  
Rollback becomes difficult

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like bad application code  
Appears like infrastructure outage  
Seems like DNS issue  
Monitoring shows healthy inactive environment

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

manual environment updates  
untracked configuration drift  
database schema mismatch  
missing secrets or certificates  
incomplete environment parity checks

---

# First Checks

Fast checks engineers should perform.

**Examples**:

config comparison between blue and green  
database schema versions  
environment variable differences  
secret and certificate validation  
dependency readiness checks

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

deployment comparison reports  
config drift alerts  
switch-over event logs  
service startup failures  
post-cutover error dashboards

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

immutable infrastructure  
automated parity validation  
full environment drift checks  
standardized deployment templates  
pre-cutover smoke testing

---

<a href="../../categories/deployment/deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>