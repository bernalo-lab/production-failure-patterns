# Pattern: Hidden Dependency Global Outage

## Description

**Hidden Dependency Global Outage** happens when an undocumented or poorly understood shared dependency fails, causing widespread impact across many unrelated services.

These failures are dangerous because engineers often do not realise the dependency even exists until production breaks.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

multiple unrelated services failing simultaneously  
unexpected cross-team incident escalation  
authentication and payments both failing  
global latency spikes without obvious source  
widespread timeout patterns across platforms

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like simultaneous independent incidents  
appears like traffic spike  
blamed on deployment failures  
seems like network instability  
appears as application regression

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

shared DNS provider failure  
hidden authentication dependency  
centralized config service outage  
third-party certificate authority disruption  
undocumented shared infrastructure dependency

---

# First Checks

Fast checks engineers should perform.

**Examples**:

map shared failing dependencies  
review recent provider incidents  
inspect cross-service common paths  
verify dependency ownership boundaries  
check hidden internal platform services

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

cross-service failure correlation  
shared dependency health checks  
provider outage notifications  
distributed tracing across services  
dependency topology maps

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

dependency mapping discipline  
shared service ownership clarity  
resilience testing for hidden dependencies  
dependency blast radius reviews  
cross-team architecture visibility

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>