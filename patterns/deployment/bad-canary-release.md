# Pattern: Bad Canary Release

## Description

A **Bad Canary Release** happens when a partial rollout intended to safely test new code introduces failures, but detection is delayed, ignored, or misinterpreted, allowing the bad release to spread to production.

Instead of limiting blast radius, the canary becomes the source of a wider outage because monitoring, rollback triggers, or success criteria were weak.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

Error rate increases after release  
Latency spikes on a subset of traffic  
Only specific regions or users affected  
Gradual production degradation  
Rollback required after expansion

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like random user errors  
Appears like dependency instability  
Seems like traffic imbalance  
Monitoring shows partial healthy status

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

poor canary success criteria  
insufficient monitoring coverage  
too much traffic routed too quickly  
hidden config differences  
manual approval mistakes

---

# First Checks

Fast checks engineers should perform.

**Examples**:

recent deployment history  
canary traffic percentage  
error rates by deployment group  
comparison between old and new version  
rollback readiness

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

deployment rollout logs  
version-specific error metrics  
latency comparison dashboards  
release pipeline events  
rollback event history

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

strict rollout guardrails  
automated rollback triggers  
clear canary success thresholds  
smaller initial blast radius  
version-aware observability

---

<a href="../../categories/deployment/deployment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>