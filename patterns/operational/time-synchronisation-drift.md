# Pattern: Time Synchronisation Drift

## Description

Time Synchronisation Drift occurs when servers or services have inconsistent system clocks.

In distributed systems, time consistency is critical for logging, tracing, authentication, and coordination between services. When clocks drift apart, logs become misaligned and debugging becomes extremely difficult.

---

# Typical Symptoms

**Examples**:

logs appearing out of order
distributed traces broken
authentication failures
inconsistent timestamps between systems
delayed scheduled tasks

---

Common Misleading Signals

**Examples**:

looks like request latency issue
appears like trace corruption
suggests logging bug
monitoring timelines inconsistent

---

# Likely Root Causes

**Examples**:

NTP service failure
incorrect time configuration
container host clock drift
virtual machine time issues
cloud instance synchronisation failure

---

# First Checks

**Examples**:

check system time on affected hosts
verify NTP status
inspect container host clocks
compare timestamps across services
check synchronisation services

---

# Useful Signals

**Examples**:

NTP logs
system clock metrics
distributed trace timestamps
authentication logs
infrastructure health metrics

---

# Prevention

**Examples**:

reliable NTP infrastructure
clock drift monitoring
time synchronisation alerts
consistent host configuration
automated time checks

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>