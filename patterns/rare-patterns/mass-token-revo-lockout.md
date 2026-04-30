# Pattern: Mass Token Revocation Lockout

## Description

**Mass Token Revocation Lockout** happens when a large-scale token invalidation event revokes active sessions across users, services, or platforms, causing sudden access failures and widespread authentication disruption.

This is especially dangerous during secret rotation, IAM incidents, or emergency security response actions.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden global login failures  
API authentication rejected across services  
users repeatedly forced to re-authenticate  
service-to-service authorization failures  
access denied errors across environments

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like identity provider outage  
appears like network failure  
blamed on OAuth provider issue  
seems like application deployment failure  
appears as random access instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

accidental global token revocation  
secret rotation without staged rollout  
incorrect IAM policy refresh  
emergency credential invalidation  
authentication cache inconsistency

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review token revocation events  
verify secret rotation history  
inspect authentication provider logs  
check token cache refresh behavior  
confirm IAM policy propagation status

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

authentication rejection logs  
identity provider audit events  
token validation failures  
session invalidation metrics  
IAM propagation status logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

staged secret rotation  
safe token revocation controls  
session invalidation testing  
rollback path for auth changes  
clear IAM propagation monitoring

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>