# Pattern: Shadow Feature Flag Catastrophe

## Description

**Shadow Feature Flag Catastrophe** happens when hidden, forgotten, or poorly controlled feature flags unexpectedly activate or conflict, causing major production instability.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

unexpected feature behaviour  
sudden production instability  
users seeing inconsistent experiences  
random feature toggles across regions  
unexplained system behaviour changes

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like deployment issue  
appears like frontend bug  
blamed on user configuration  
seems like A/B testing issue  
appears as random regression

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

forgotten feature flags  
conflicting flag combinations  
improper flag rollout  
lack of flag governance  
manual flag changes without tracking

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review active feature flags  
inspect recent flag changes  
verify rollout rules  
check flag dependencies  
compare environment configurations

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

feature flag audit logs  
configuration change history  
user experience discrepancies  
deployment vs flag change timeline  
application behaviour logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

feature flag lifecycle management  
clear flag ownership  
automated flag cleanup  
flag change auditing  
safe rollout strategies

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>