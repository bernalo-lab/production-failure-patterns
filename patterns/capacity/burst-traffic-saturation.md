# Pattern: Burst Traffic Saturation

## Description

**Burst Traffic Saturation** happens when sudden spikes in traffic exceed system capacity faster than scaling or protection mechanisms can respond.

This creates rapid latency increases, request failures, and cascading retries that can overwhelm otherwise healthy services.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sharp latency spike  
sudden 5xx error increase  
request queues filling rapidly  
autoscaling triggered too late  
timeouts across multiple services

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like DDoS attack  
appears like dependency outage  
seems like code regression  
blamed on bad deployment  
appears as random infrastructure instability

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

unexpected customer traffic surge  
marketing campaign spikes  
missing rate limits  
slow autoscaling response  
cache miss storms

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review incoming request volume  
check autoscaler activity  
inspect cache hit ratios  
validate rate limiting behaviour  
identify traffic source concentration

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

request rate dashboards  
autoscaling event logs  
queue depth metrics  
cache miss ratios  
load balancer traffic metrics

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

rate limiting  
pre-scaling for known events  
burst load testing  
faster autoscaler policies  
circuit breakers

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>