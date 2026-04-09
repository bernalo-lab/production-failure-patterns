# Pattern: DNS Resolution Failure

## Description

DNS Resolution Failure occurs when services cannot resolve the hostname of a dependency or internal service.

Without proper DNS resolution, applications cannot locate the IP address of required services. This results in connection failures even though the target system may still be healthy.

DNS failures can disrupt large portions of distributed systems.

---

## Typical Symptoms

Engineers may observe:

Sudden connection failures
Service discovery errors
High failure rate for outbound requests
“Host not found” errors
Connection retries increasing rapidly

---

## Common Misleading Signals

The issue may appear as:

Service outage
Network connectivity problems
Infrastructure failure

However, the actual problem is often DNS resolution failing upstream.

---

## Likely Root Causes

Typical causes include:

DNS server outage
Misconfigured DNS records
Expired DNS entries
Incorrect service discovery configuration
Network restrictions blocking DNS traffic

---

## First Checks

Engineers should check:

DNS resolution from affected hosts
Service discovery configuration
DNS server health
Recent DNS record changes
TTL values

---

## Useful Signals

Look for:

DNS query errors
Connection error logs
Network traces
Service discovery logs

---

## Prevention

**DNS Redundancy**
Use multiple DNS providers or resolvers.

**Health Monitoring**
Continuously monitor DNS resolution.

**Short TTLs**
Allow faster DNS updates.

**Fallback Mechanisms**
Maintain secondary endpoints when possible.

---

<a href="../../categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>