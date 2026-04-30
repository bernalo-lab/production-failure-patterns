# Pattern: BGP Route Leak Blackhole

## Description

**BGP Route Leak Blackhole** happens when incorrect routing information is propagated across the internet, causing traffic to be misrouted, intercepted, or completely dropped.

This can lead to large-scale outages affecting multiple regions, providers, and services simultaneously.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden global service unreachability  
traffic drops across regions  
increased packet loss  
intermittent connectivity failures  
complete outage for specific providers

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like application outage  
appears like DDoS attack  
blamed on cloud provider failure  
seems like DNS issue  
appears as random network instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

misconfigured BGP announcements  
route leak from ISP  
incorrect prefix advertisement  
malicious route hijacking  
upstream provider misconfiguration

---

# First Checks

Fast checks engineers should perform.

**Examples**:

verify network routes via traceroute  
check global BGP monitoring tools  
compare connectivity across ISPs  
inspect provider status updates  
validate route announcements

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

network latency metrics  
packet loss indicators  
traceroute inconsistencies  
BGP monitoring feeds  
ISP status alerts

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

multi-provider network redundancy  
BGP route filtering policies  
external route monitoring  
failover routing strategies  
provider diversity planning

---

<a href="../../categories/rare-patterns/rare-patterns.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>