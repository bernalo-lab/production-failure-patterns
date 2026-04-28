# Pattern: Config Drift Across Environments

## Description

**Config Drift Across Environments** happens when application, infrastructure, or platform configuration gradually becomes inconsistent between environments such as development, staging, and production.

This creates hidden differences where software behaves correctly in one environment but fails unexpectedly in another, making testing unreliable and production incidents difficult to predict.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

works in staging but fails in production
unexpected behaviour after deployment
missing feature flags in one environment
different timeout behaviour across environments
inconsistent database or API responses

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like code regression
appears like dependency failure
seems like data corruption
blamed on deployment timing
appears as random intermittent issue

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

manual configuration changes
missing infrastructure-as-code controls
environment-specific overrides
outdated secret values
inconsistent feature flag settings

---

# First Checks

Fast checks engineers should perform.

**Examples**:

compare config files across environments
review recent manual changes
validate feature flags
check secrets and environment variables
inspect infrastructure definitions

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

configuration diff reports
deployment history logs
environment variable audits
feature flag dashboards
infrastructure drift detection tools

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

infrastructure as code
configuration version control
automated drift detection
immutable deployments
environment parity checks

---

<a href="../../categories/configuration/configuration.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;"><<Back</a>