# Category: Security & Access Failure Patterns

---

# 01. Pattern: Secret Rotation

## Description

**Secret Rotation** Failure occurs when application credentials such as API keys, database passwords, certificates, or encryption secrets are rotated incorrectly or inconsistently across systems.

This often causes sudden authentication failures, service outages, and cascading dependency failures when services continue using expired or mismatched secrets.

---

# 02. Pattern: IAM Permission Drift

## Description

**IAM Permission Drift** occurs when access permissions gradually diverge from intended policy due to manual changes, inconsistent deployments, or unmanaged exceptions.

This creates production outages when services suddenly lose required access or gain unintended permissions that trigger security controls.

---

# 03. Pattern: Privilege Escalation Lockout

## Description

**Privilege Escalation Lockout** occurs when administrative access paths fail due to broken elevation controls, expired emergency access, or incorrect privilege boundaries.

This can prevent responders from accessing critical systems during incidents, increasing outage duration and operational risk.

---

# 04. Pattern: Token Expiry Cascade

## Description

**Token Expiry Cascade** occurs when authentication or service tokens expire simultaneously across multiple services, causing widespread authorization failures and retry storms.

This commonly happens in distributed systems where token refresh mechanisms fail, refresh windows are too narrow, or shared dependencies rely on synchronized expiry schedules.

---

# 05. Pattern: Certificate Chain Trust

## Description

**Certificate Chain Trust** Failure occurs when systems cannot validate TLS/SSL certificates because the certificate chain is incomplete, expired, misconfigured, or issued by an untrusted authority.

This causes secure connections to fail and can create widespread outages across internal services and external integrations.

---

# 06. Pattern: WAF False Positive Blocking

## Description

**WAF False Positive Blocking** occurs when legitimate application traffic is incorrectly blocked by Web Application Firewall rules that classify safe requests as malicious.

This can create sudden customer-facing outages and is especially common after rule updates or stricter security policies.

---

# 07. Pattern: DDoS Protection Misfire

## Description

**DDoS Protection Misfire** occurs when defensive systems incorrectly classify legitimate traffic as attack traffic and trigger aggressive mitigation actions.

This can cause self-inflicted outages where protection systems become the source of service disruption.

---

# 08. Pattern: Security Group Misconfiguration

## Description

**Security Group Misconfiguration** occurs when network access rules are incorrectly configured, blocking required traffic or unintentionally exposing services to the wrong sources.

This often causes sudden connectivity failures between services, failed deployments, and hard-to-diagnose production incidents.

---

# 09. Pattern: Firewall Rule Drift

## Description

**Firewall Rule Drift** occurs when firewall policies gradually diverge from intended design due to manual changes, temporary exceptions, or inconsistent deployments.

This can silently introduce outages by blocking legitimate traffic or create security risks by leaving unintended access paths open.

---

# 10. Pattern: OAuth Provider

## Description

**OAuth Provider** Failure occurs when the identity provider responsible for authentication or authorization becomes unavailable, degraded, or returns invalid responses.

This creates widespread login failures, broken service access, and cascading disruption across systems that depend on centralized authentication.

---
