# Pattern: Clock Skew Breaking Coordination

## Description

**Clock Skew Breaking Coordination** happens when system clocks drift between servers, causing distributed coordination logic to fail.

This affects leader elections, token expiry, retries, distributed locks, and event ordering because many systems assume reasonably synchronised time.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

authentication tokens fail unexpectedly  
distributed locks behave incorrectly  
duplicate scheduled jobs  
unexpected failovers  
message ordering problems

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like auth system issue  
appears like database lock problem  
seems like race condition  
blamed on deployment regression  
appears as random distributed bug

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

NTP sync failures  
virtual machine clock drift  
misconfigured time servers  
host resource starvation  
manual time configuration errors

---

# First Checks

Fast checks engineers should perform.

**Examples**:

compare system times across nodes  
verify NTP service health  
inspect authentication timestamps  
check lock lease durations  
review failover timing logs

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

NTP sync logs  
timestamp mismatch events  
token validation failures  
distributed lock expiry logs  
node time comparison dashboards

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

reliable NTP configuration  
clock drift monitoring  
lease safety margins  
timestamp validation checks  
time sync alerting

---

<a href="../../categories/configuration/configuration.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
