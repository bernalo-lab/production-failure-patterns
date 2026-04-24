# Pattern: Certificate Chain Trust Failure

## Description

**Certificate Chain Trust** Failure occurs when systems cannot validate TLS/SSL certificates because the certificate chain is incomplete, expired, misconfigured, or issued by an untrusted authority.

This causes secure connections to fail and can create widespread outages across internal services and external integrations.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

TLS handshake failures  
SSL validation errors  
Service connection failures  
Dependency timeouts  
Certificate trust warnings

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like network outage  
Appears like DNS issue  
Seems like dependency failure  
Monitoring suggests firewall problem

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

expired certificates  
missing intermediate certificates  
incorrect certificate deployment  
untrusted certificate authority  
hostname mismatch

---

# First Checks

Fast checks engineers should perform.

**Examples**:

certificate expiry dates  
certificate chain validation  
hostname verification  
recent certificate changes  
CA trust store status

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

TLS handshake error logs  
certificate validation failures  
SSL monitoring alerts  
dependency connection logs  
certificate expiry dashboards

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

certificate expiry monitoring  
automated renewal  
full chain validation tests  
centralized certificate management  
pre-deployment trust checks

---

<a href="../../categories/security/security.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>