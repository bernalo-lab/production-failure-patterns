# Pattern: Service Discovery Failure

## Description

**Service Discovery Failure** happens when services cannot correctly locate or resolve other services required for communication.

This breaks internal traffic routing and causes partial or full outages even when the target services themselves are healthy.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden connection failures between services  
timeouts despite healthy dependencies  
intermittent request routing failures  
traffic sent to wrong instances  
service startup failures

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like DNS outage  
appears like dependency crash  
seems like network packet loss  
blamed on application bugs  
appears as infrastructure instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

stale service registry entries  
DNS propagation delays  
failed health checks  
misconfigured service mesh  
registration heartbeat failures

---

# First Checks

Fast checks engineers should perform.

**Examples**:

validate service registration status  
check DNS resolution results  
review health check outcomes  
inspect service mesh routes  
compare healthy vs failing instances

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

service registry logs  
DNS query metrics  
health check failures  
routing table inspection  
connection timeout traces

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

robust health checks  
registry consistency monitoring  
DNS TTL management  
fallback service endpoints  
service discovery validation tests

---

<a href="../../categories/configuration/configuration.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
