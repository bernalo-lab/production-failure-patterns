# Pattern: Security Group Misconfiguration

## Description

**Security Group Misconfiguration** occurs when network access rules are incorrectly configured, blocking required traffic or unintentionally exposing services to the wrong sources.

This often causes sudden connectivity failures between services, failed deployments, and hard-to-diagnose production incidents.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Service-to-service connection failures  
Database access timeouts  
Application deployment failures  
Unexpected connection refused errors  
Intermittent dependency outages

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like application bug  
Appears like database outage  
Seems like DNS failure  
Monitoring suggests downstream instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

incorrect inbound rules  
wrong outbound restrictions  
manual security group edits  
environment drift  
incomplete infrastructure deployment

---

# First Checks

Fast checks engineers should perform.

**Examples**:

recent security group changes  
inbound and outbound rules  
port and protocol validation  
source and destination restrictions  
deployment change history

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

connection timeout logs  
network flow logs  
security group audit trails  
failed health checks  
port connectivity validation results

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

infrastructure-as-code enforcement  
security group drift detection  
change approval workflows  
network access testing  
automated policy validation

---

<a href="../../categories/security/security.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>