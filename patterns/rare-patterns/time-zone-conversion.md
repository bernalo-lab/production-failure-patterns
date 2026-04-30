# Pattern: Time Zone Conversion Catastrophe

## Description

**Time Zone Conversion Catastrophe** happens when incorrect timezone handling causes systems to execute business logic at the wrong time, often affecting billing, scheduling, authentication, or regulatory workflows.

These failures are especially dangerous during daylight saving transitions and cross-region operations.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

jobs running at incorrect times  
duplicate scheduled executions  
missed billing windows  
authentication token expiry confusion  
incorrect compliance reporting timestamps

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like scheduler bug  
appears like user timezone issue  
blamed on cron misconfiguration  
seems like application race condition  
appears as isolated timing anomaly

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

UTC and local time mismatch  
daylight saving transition bug  
hardcoded timezone assumptions  
database timestamp inconsistency  
cross-region conversion logic failure

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify timezone conversion logic  
inspect DST transition timing  
review scheduler timezone settings  
check database timestamp storage  
compare UTC and local execution times

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

scheduler execution history  
application timestamp logs  
billing event timelines  
authentication expiry events  
database timezone metadata

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

UTC-first architecture  
timezone-safe scheduling  
DST transition testing  
explicit timezone observability  
validated regional conversion rules

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>