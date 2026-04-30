# Pattern: Certificate Revocation Failure

## Description

**Certificate Revocation Failure** happens when systems fail to properly check revoked certificates or cannot reach revocation services like CRL or OCSP, causing trust failures or unintended access blocks.

This often creates authentication outages and unexpected TLS failures across production systems.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden TLS handshake failures  
authentication service outage  
certificate trust errors  
users locked out of services  
intermittent secure connection failures

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

appears like expired certificate  
looks like network issue  
blamed on identity provider outage  
seems like proxy failure  
appears as firewall restriction

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

OCSP responder unavailable  
CRL distribution point unreachable  
incorrect revocation policy enforcement  
stale revocation cache  
unexpected CA revocation event

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify certificate revocation status  
test OCSP and CRL endpoint access  
inspect TLS handshake logs  
check recent CA revocation notices  
validate trust store configuration

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

TLS handshake failure logs  
certificate validation events  
OCSP responder health  
CRL fetch errors  
identity provider authentication logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

resilient OCSP fallback design  
trust store monitoring  
certificate lifecycle audits  
revocation endpoint health checks  
graceful failure policy design

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>