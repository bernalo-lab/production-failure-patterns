# Pattern: Environment Variable Mismatch

## Description

**Environment Variable Mismatch** happens when required environment variables differ across services, containers, or environments, causing unexpected behaviour or outright failures.

Because environment variables often control critical runtime behaviour, even a small mismatch can break authentication, service communication, or feature execution.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

service starts but fails requests
authentication failures after deploy
unexpected connection errors
feature works for one service but not another
application crashes during startup

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like network issue
appears like database outage
seems like bad deployment
blamed on dependency instability
appears as random application bug

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

missing environment variables
incorrect secret injection
stale deployment manifests
manual copy-paste mistakes
different CI/CD pipeline settings

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify runtime environment variables
compare deployment manifests
check secret injection process
validate application startup logs
review recent deployment changes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

startup failure logs
container environment inspection
deployment manifests
secret manager audit logs
application configuration output

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

environment validation checks
startup configuration validation
centralised secret management
CI/CD config verification
required variable enforcement

---

<a href="../../categories/configuration/configuration.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;"><<Back</a>