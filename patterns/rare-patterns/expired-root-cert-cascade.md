# Pattern: Expired Root Certificate Cascade

## Description

**Expired Root Certificate Cascade** happens when a widely trusted root certificate expires, causing dependent services, clients, and integrations to suddenly fail trust validation across large parts of the system.

This often creates global outages with confusing downstream failures.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden TLS connection failures  
authentication provider outages  
API integrations failing globally  
certificate validation errors across services  
unexpected customer login failures

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like dependency outage  
appears like DNS issue  
blamed on network instability  
seems like application release failure  
appears as random TLS breakage

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

expired trusted root certificate  
outdated trust store on clients  
certificate chain validation mismatch  
legacy systems using old trust bundles  
missed certificate lifecycle monitoring

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify certificate chain validity  
inspect root CA expiration dates  
check trust store versions  
review recent TLS failures  
validate dependency certificate status

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

TLS handshake failures  
certificate validation logs  
authentication provider alerts  
trust store version reports  
dependency connection failures

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

certificate lifecycle monitoring  
automated trust store updates  
expiration alerting  
dependency certificate audits  
staged certificate rotation testing

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>