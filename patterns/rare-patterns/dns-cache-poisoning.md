# Pattern: DNS Cache Poisoning

## Description

**DNS Cache Poisoning** happens when incorrect or malicious DNS records are cached by resolvers, causing services to resolve dependencies to the wrong destination.

This can create widespread outages, traffic blackholes, and severe security risks across internal and external systems.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden service connection failures  
traffic routed to incorrect hosts  
authentication failures across services  
intermittent dependency timeouts  
unexpected SSL certificate mismatches

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like dependency outage  
appears like TLS certificate issue  
blamed on firewall changes  
seems like application bug  
appears as random network instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

compromised DNS resolver  
stale poisoned DNS cache  
incorrect DNS zone propagation  
resolver trust weakness  
malicious spoofed DNS responses

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify DNS resolution results  
compare internal and external resolver responses  
inspect resolver cache entries  
check certificate hostnames  
validate authoritative DNS records

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

DNS query logs  
resolver cache inspection  
service connection failure logs  
certificate validation failures  
network route tracing

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

DNSSEC adoption  
resolver hardening  
short safe TTL policies  
resolver monitoring  
multi-resolver validation

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>