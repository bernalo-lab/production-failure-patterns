# Pattern: Bad Configuration Deployment

## Description

A **Bad Configuration Deployment** occurs when a configuration change introduces incorrect behaviour, instability, or service failure without requiring a code change.

This pattern appears in production systems because configuration often controls feature flags, connection settings, timeouts, resource limits, routing rules, and dependency endpoints. A small mistake in these settings can cause immediate and widespread impact, especially when rolled out across many instances at once.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- Sudden error rate increase after rollout
- Latency spike
- Service startup failures
- Dependency connection failures
- Unexpected behaviour across multiple instances
- Need for urgent rollback

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like code deployment issue
- Appears like dependency outage
- Monitoring alerts from downstream service
- Seems like infrastructure failure
- Appears like application bug

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- Incorrect environment variable value
- Misconfigured timeout or retry settings
- Wrong endpoint or credential
- Invalid resource limits
- Broken routing or feature flag configuration
- Incomplete configuration validation

---

## First Checks

Fast checks engineers should perform.

Examples:

- Recent configuration changes
- Differences between healthy and failing instances
- Environment variable values
- Rollout timeline
- Dependency endpoints and credentials
- Startup logs after configuration load

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- config load error logs
- deployment timeline correlation
- startup failure logs
- environment diff checks
- sudden metric shifts after rollout
- service health check failures

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- configuration validation
- staged rollouts
- change approval workflows
- config diff checks
- safe defaults
- rollback automation