# Pattern: Token Expiry Cascade

## Description

**Token Expiry Cascade** occurs when authentication or service tokens expire simultaneously across multiple services, causing widespread authorization failures and retry storms.

This commonly happens in distributed systems where token refresh mechanisms fail, refresh windows are too narrow, or shared dependencies rely on synchronized expiry schedules.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

401 unauthorized errors  
Authentication failures across services  
Retry storms  
Service-to-service communication failures  
Sudden spike in failed background jobs

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like dependency outage  
Appears like IAM permission issue  
Seems like secret rotation failure  
Monitoring suggests downstream instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

failed token refresh logic  
synchronized token expiration  
clock drift between systems  
stale refresh credentials  
identity provider instability

---

# First Checks

Fast checks engineers should perform.

**Examples**:

token expiration timestamps  
refresh token validity  
identity provider health  
clock synchronization status  
recent auth configuration changes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

401/403 error logs  
authentication service metrics  
token refresh failures  
identity provider logs  
retry and backoff patterns

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

staggered token refresh windows  
grace periods before expiry  
clock synchronization monitoring  
token refresh validation  
fallback authentication paths

---

<a href="../../categories/security/security.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>