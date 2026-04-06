# Pattern: DNS Resolution Failure

## Description

A **DNS Resolution Failure** occurs when services or clients cannot correctly resolve hostnames into IP addresses.

This pattern appears in production systems when DNS servers fail, records expire unexpectedly, service discovery breaks, or clients cache stale records. Since many services depend on DNS for locating internal and external dependencies, even a small DNS issue can cause widespread communication failures across the system.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- Sudden connection failures
- Increased error rates across multiple services
- Service startup failures
- Intermittent request failures
- Requests failing only for specific dependencies
- Healthy service instances appearing unreachable

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like dependency outage
- Appears like network partition
- Monitoring alerts from application layer
- Seems like load balancer issue
- Appears like service crash

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- DNS server outage
- Expired or missing DNS records
- Misconfigured service discovery
- Stale DNS cache on clients
- Incorrect TTL settings
- Split-horizon DNS issues

---

## First Checks

Fast checks engineers should perform.

Examples:

- DNS lookup results for affected hostnames
- DNS server health
- TTL and record configuration
- Client-side DNS cache behaviour
- Service discovery registration
- Differences between working and failing hosts

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- name resolution error logs
- DNS query failure metrics
- service discovery logs
- failed hostname lookups
- dependency connection error logs
- resolver timeout metrics

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- redundant DNS resolvers
- sensible TTL settings
- DNS health monitoring
- service discovery validation
- fallback resolvers
- regular failover testing

---

<a href="../../categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
