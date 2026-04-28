# Pattern: Stale Configuration Cache

## Description

**Stale Configuration Cache** happens when services continue using outdated configuration because cache refreshes fail, are delayed, or are never triggered.

This creates hidden inconsistencies where some systems use new settings while others continue operating with old values.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

feature flags behave inconsistently  
policy updates do not apply  
old endpoints still being used  
security changes ignored  
partial system behaviour after config update

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like deployment inconsistency  
appears like code regression  
seems like regional failure  
blamed on user behaviour  
appears as random configuration issue

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

cache invalidation failures  
refresh jobs not running  
stuck long-lived processes  
event-driven refresh failure  
misconfigured cache TTL values

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify current active config version  
check cache refresh jobs  
review invalidation events  
inspect process restart history  
compare expected vs actual values

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

config version logs  
cache invalidation events  
refresh scheduler metrics  
feature flag audit logs  
service startup configuration output

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

explicit cache invalidation  
versioned configuration checks  
forced refresh mechanisms  
short safe TTLs  
runtime config visibility

---

<a href="../../categories/configuration/configuration.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
