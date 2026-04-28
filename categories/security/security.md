# Category: Security & Access Failure Patterns

## Decsription
These failures create incidents through authentication, permissions, certificates, secrets, and security controls. They often appear as outages even though the root cause is access denial, trust failure, or security misconfiguration.

---

# 01. Pattern: Secret Rotation

## Description

<a href="../../patterns/security/secret-rotation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Secret Rotation**</a> Failure occurs when application credentials such as API keys, database passwords, certificates, or encryption secrets are rotated incorrectly or inconsistently across systems.

This often causes sudden authentication failures, service outages, and cascading dependency failures when services continue using expired or mismatched secrets.

---

# 02. Pattern: IAM Permission Drift

## Description

<a href="../../patterns/security/iam-permission-drift.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**IAM Permission Drift**</a> occurs when access permissions gradually diverge from intended policy due to manual changes, inconsistent deployments, or unmanaged exceptions.

This creates production outages when services suddenly lose required access or gain unintended permissions that trigger security controls.

---

# 03. Pattern: Privilege Escalation Lockout

## Description

<a href="../../patterns/security/privilege-escalation-lock.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Privilege Escalation Lockout**</a> occurs when administrative access paths fail due to broken elevation controls, expired emergency access, or incorrect privilege boundaries.

This can prevent responders from accessing critical systems during incidents, increasing outage duration and operational risk.

---

# 04. Pattern: Token Expiry Cascade

## Description

<a href="../../patterns/security/token-expiry-cascade.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Token Expiry Cascade**</a> occurs when authentication or service tokens expire simultaneously across multiple services, causing widespread authorization failures and retry storms.

This commonly happens in distributed systems where token refresh mechanisms fail, refresh windows are too narrow, or shared dependencies rely on synchronized expiry schedules.

---

# 05. Pattern: Certificate Chain Trust

## Description

<a href="../../patterns/security/certificate-chain-trust.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Certificate Chain Trust**</a> Failure occurs when systems cannot validate TLS/SSL certificates because the certificate chain is incomplete, expired, misconfigured, or issued by an untrusted authority.

This causes secure connections to fail and can create widespread outages across internal services and external integrations.

---

# 06. Pattern: WAF False Positive Blocking

## Description

<a href="../../patterns/security/waf-false-positive-block.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**WAF False Positive Blocking**</a> occurs when legitimate application traffic is incorrectly blocked by Web Application Firewall rules that classify safe requests as malicious.

This can create sudden customer-facing outages and is especially common after rule updates or stricter security policies.

---

# 07. Pattern: DDoS Protection Misfire

## Description

<a href="../../patterns/security/ddos-protection-misfire.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**DDoS Protection Misfire**</a> occurs when defensive systems incorrectly classify legitimate traffic as attack traffic and trigger aggressive mitigation actions.

This can cause self-inflicted outages where protection systems become the source of service disruption.

---

# 08. Pattern: Security Group Misconfiguration

## Description

<a href="../../patterns/security/security-group-misconfiguration.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Security Group Misconfiguration**</a> occurs when network access rules are incorrectly configured, blocking required traffic or unintentionally exposing services to the wrong sources.

This often causes sudden connectivity failures between services, failed deployments, and hard-to-diagnose production incidents.

---

# 09. Pattern: Firewall Rule Drift

## Description

<a href="../../patterns/security/firewall-rule-drift.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Firewall Rule Drift**</a> occurs when firewall policies gradually diverge from intended design due to manual changes, temporary exceptions, or inconsistent deployments.

This can silently introduce outages by blocking legitimate traffic or create security risks by leaving unintended access paths open.

---

# 10. Pattern: OAuth Provider

## Description

<a href="../../patterns/security/oauth-provider.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**OAuth Provider**</a> Failure occurs when the identity provider responsible for authentication or authorization becomes unavailable, degraded, or returns invalid responses.

This creates widespread login failures, broken service access, and cascading disruption across systems that depend on centralized authentication.

----

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
