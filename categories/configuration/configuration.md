# Category: Configuration & Control Plane Failure Patterns

## Description
These failures come from hidden configuration mismatches, stale settings, control plane outages, and coordination problems between services or infrastructure. They are often difficult to detect because systems may appear healthy while behaviour becomes inconsistent.

---

# 01. Pattern: Config Drift Across Environments

## Description

<a href="../../patterns/configuration/config-drift-across-env.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Config Drift Across Environments**</a> happens when application, infrastructure, or platform configuration gradually becomes inconsistent between environments such as development, staging, and production.

This creates hidden differences where software behaves correctly in one environment but fails unexpectedly in another, making testing unreliable and production incidents difficult to predict.

---

# 02. Pattern: Environment Variable Mismatch

## Description

<a href="../../patterns/configuration/env-variable-mismatch.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Environment Variable Mismatch**</a> happens when required environment variables differ across services, containers, or environments, causing unexpected behaviour or outright failures.

Because environment variables often control critical runtime behaviour, even a small mismatch can break authentication, service communication, or feature execution.

---

# 03. Pattern: Default Configuration Override Failure

## Description

<a href="../../patterns/configuration/default-config-override.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Default Configuration Override Failure**</a> happens when expected custom configuration is not applied and the system silently falls back to unsafe or incorrect default settings.

This often creates subtle production issues because the application still runs, but with behaviour that operators did not intend.

---

# 04. Pattern: Regional Configuration Inconsistency

## Description

<a href="../../patterns/configuration/regional-config-inconsistency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Regional Configuration Inconsistency** happens when different regions run different configuration values, policies, or operational settings, creating inconsistent system behaviour across geography.

This is especially dangerous in multi-region systems where traffic shifts can expose hidden failures only in specific locations.

---

# 05. Pattern: Control Plane API Failure

## Description

<a href="../../patterns/configuration/control-plane-api.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Control Plane API Failure**</a> happens when the management layer responsible for orchestrating infrastructure, services, or platform resources becomes unavailable, slow, or inconsistent.

Unlike data plane failures, workloads may continue temporarily, but scaling, scheduling, deployments, failover, and operational changes start failing, often creating delayed production incidents.

---

# 06. Pattern: Service Discovery Failure

## Description

<a href="../../patterns/configuration/service-discovery.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Service Discovery Failure**</a> happens when services cannot correctly locate or resolve other services required for communication.

This breaks internal traffic routing and causes partial or full outages even when the target services themselves are healthy.

---

# 07. Pattern: Leader Election Failure

## Description

<a href="../../patterns/configuration/leader-election.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Leader Election Failure**</a> happens when distributed systems fail to correctly assign or maintain a single active leader responsible for coordination tasks.

This can create split-brain behaviour, stalled processing, or duplicate operations depending on whether no leader or multiple leaders emerge.

---

# 08. Pattern: Clock Skew Breaking Coordination

## Description

<a href="../../patterns/configuration/clock-skew-breaking-coordn.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Clock Skew Breaking Coordination**</a> happens when system clocks drift between servers, causing distributed coordination logic to fail.

This affects leader elections, token expiry, retries, distributed locks, and event ordering because many systems assume reasonably synchronised time.

---

# 09. Pattern: Stale Configuration Cache

## Description

<a href="../../patterns/configuration/stale-configuration-cache.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Stale Configuration Cache**</a> happens when services continue using outdated configuration because cache refreshes fail, are delayed, or are never triggered.

This creates hidden inconsistencies where some systems use new settings while others continue operating with old values.

---

# 10. Pattern: Configuration Rollout Race Condition

## Description

<a href="../../patterns/configuration/config-rollout-race-condn.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Configuration Rollout Race Condition**</a> happens when configuration changes are applied across systems in the wrong order, causing temporary incompatibility and outages.

Even correct configuration can fail if dependent services update before prerequisites are ready.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>

