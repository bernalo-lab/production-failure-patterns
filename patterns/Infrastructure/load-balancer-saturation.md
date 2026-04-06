# Pattern: Load Balancer Saturation

## Description

**Load Balancer Saturation** occurs when a load balancer becomes a bottleneck and can no longer efficiently distribute incoming traffic.

This pattern appears in production systems when traffic exceeds capacity, connection limits are reached, health checks become unstable, or the load balancer itself runs out of resources. Even when backend services are healthy, a saturated load balancer can create system-wide latency, dropped requests, and uneven traffic distribution.

---

## Typical Symptoms

What engineers usually observe.

Examples:

- Latency spike before requests reach backend services
- Error rate increase at entry point
- Dropped or reset connections
- Uneven traffic distribution across instances
- Healthy backends receiving reduced traffic
- Sudden increase in 502, 503, or 504 responses

---

## Common Misleading Signals

Signals that often send engineers down the wrong path.

Examples:

- Looks like backend service failure
- Appears like traffic spike
- Monitoring alerts from downstream service
- Seems like application slowdown
- Appears like network congestion

---

## Likely Root Causes

Typical reasons this pattern occurs.

Examples:

- Traffic surge beyond load balancer capacity
- Connection table exhaustion
- Misconfigured health checks
- Insufficient scaling of ingress layer
- SSL termination overload
- Session persistence imbalance

---

## First Checks

Fast checks engineers should perform.

Examples:

- Load balancer CPU and connection metrics
- Backend health check status
- Incoming traffic volume
- Error codes returned by ingress layer
- Distribution of requests across instances
- Recent configuration changes

---

## Useful Signals

Logs, metrics, or traces that help confirm the issue.

Examples:

- load balancer error logs
- connection saturation metrics
- backend health check failures
- request drop metrics
- ingress latency metrics
- frontend-to-backend routing traces

---

## Prevention

What can reduce the likelihood of this pattern.

Examples:

- horizontal scaling of ingress layer
- connection limit monitoring
- rate limiting
- health check tuning
- traffic shaping
- load testing at entry layer

---

<a href="../../categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
