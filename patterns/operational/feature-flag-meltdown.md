# Pattern: Feature Flag Meltdown

## Description

A **Feature Flag Meltdown** occurs when enabling, disabling, or misconfiguring a feature flag causes unexpected system-wide impact.

This pattern appears in production systems because feature flags often control important code paths, traffic routing, backend calls, or expensive functionality. When a flag is rolled out too broadly or interacts badly with existing behaviour, it can trigger latency spikes, dependency overload, inconsistent behaviour, or partial outages.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- Sudden latency spike after flag change
- Error rate increase
- Uneven behaviour across users or instances
- Dependency overload
- Increased request volume on new code path
- Partial service degradation

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like bad deployment
- Appears like traffic spike
- Monitoring alerts from downstream service
- Seems like application regression
- Appears like capacity issue

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- Flag enabled for too many users at once
- New code path increases dependency load
- Conflicting feature flag combinations
- Incomplete testing of flagged behaviour
- Missing rollback guardrails
- Flag state inconsistency across instances

---

## First Checks

Fast checks engineers should perform.

Examples:

- Recent feature flag changes
- Scope of rollout
- Differences between flagged and unflagged traffic
- Dependency latency after enablement
- Error rates by cohort
- Rollback behaviour of the flag

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- feature flag audit logs
- cohort-based error metrics
- latency changes after flag enablement
- dependency traffic metrics
- trace differences by code path
- rollout timeline correlation

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- staged rollout
- feature flag governance
- cohort monitoring
- safe rollback controls
- pre-release load testing
- flag dependency review

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
