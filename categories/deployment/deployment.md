# Category: Deployment & Release Failure Patterns

---

# 01. Pattern: Bad Canary Release

## Description

A <a href="../../patterns/deployment/bad-canary-release.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Bad Canary Release**</a> happens when a partial rollout intended to safely test new code introduces failures, but detection is delayed, ignored, or misinterpreted, allowing the bad release to spread to production.

Instead of limiting blast radius, the canary becomes the source of a wider outage because monitoring, rollback triggers, or success criteria were weak.

---

# 02. Pattern: Blue-Green Deployment Drift

## Description

<a href="../../patterns/deployment/blue-green-deployment-drift.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Blue-Green Deployment Drift**</a> occurs when the blue and green environments gradually stop matching each other due to configuration differences, data mismatches, or infrastructure changes.

When traffic switches, unexpected failures occur because the standby environment is no longer truly production-ready.

---

# 03. Pattern: Rollback Failure

## Description

<a href="../../patterns/deployment/rollback-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Rollback Failure**</a> occurs when engineers attempt to revert a deployment during an incident, but the rollback itself fails or makes the outage worse.

This often happens because rollback paths are untested, state has changed, or dependencies are no longer compatible with the previous version.

---

# 04. Pattern: Partial Deployment State

## Description

<a href="../../patterns/deployment/partial-deployment-state.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Partial Deployment State**</a> occurs when only part of a deployment succeeds, leaving the system running with a mixed combination of old and new versions, incomplete resources, or inconsistent infrastructure.

This creates unpredictable behaviour because services, dependencies, or configurations are no longer aligned across the production environment.

---

# 05. Pattern: CI/CD Pipeline Failure

## Description

<a href="../../patterns/deployment/cicd-pipeline-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**CI/CD Pipeline Failure**</a> occurs when the build, test, release, or deployment automation fails and prevents safe delivery to production or introduces unstable changes.

This can block releases entirely or allow broken deployments if validation steps are skipped or bypassed.

---

# 06. Pattern: Infrastructure Drift After Deploy

## Description

<a href="../../patterns/deployment/infra-drift-after-deploy.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Infrastructure Drift After Deploy**</a> occurs when the live production environment no longer matches the intended declared infrastructure state after deployment.

This creates hidden instability because systems behave differently from what deployment automation expects.

---

# 07. Pattern: Deployment Dependency Ordering Failure

## Description

<a href="../../patterns/deployment/deployment-dependency-ordering.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Deployment Dependency Ordering Failure**</a> happens when services, infrastructure, or migrations are deployed in the wrong sequence, causing downstream systems to fail because prerequisites are not yet ready.

This often creates outages during otherwise valid releases.

---

# 08. Pattern: Helm Chart Misconfiguration

## Description

<a href="../../patterns/deployment/deployment-dependency-ordering.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Helm Chart Misconfiguration**</a> occurs when Kubernetes deployments fail or behave incorrectly because Helm chart values, templates, or release definitions are wrong.

Small configuration mistakes can create major outages across services and clusters.

---

# 09. Pattern: Terraform State Corruption

## Description

<a href="../../patterns/deployment/terraform-state-corruption.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Terraform State Corruption**</a> occurs when the Terraform state file becomes inconsistent, incomplete, locked incorrectly, or no longer reflects the real infrastructure.

This makes deployments dangerous because Terraform may destroy, recreate, or lose track of critical production resources.

---

# 10. Pattern: Partial Deployment State

## Description

<a href="../../patterns/deployment/partial-deployment-state.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Partial Deployment State**</a> occurs when only part of a deployment succeeds, leaving the system running with a mixed combination of old and new versions, incomplete resources, or inconsistent infrastructure.

This creates unpredictable behaviour because services, dependencies, or configurations are no longer aligned across the production environment.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
