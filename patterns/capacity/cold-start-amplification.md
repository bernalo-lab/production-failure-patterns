# Pattern: Cold Start Amplification

## Description

**Cold Start Amplification** happens when new instances, containers, or serverless functions take too long to become useful during traffic spikes or recovery events.

Instead of relieving pressure, startup delays increase retries, queue growth, and cascading failures across the platform.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

new instances launched but latency remains high  
queue depth grows despite scaling  
serverless invocation latency spikes  
retries increase during scaling events  
recovery takes much longer than expected

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like autoscaler failure  
appears like dependency outage  
seems like deployment issue  
blamed on network delays  
appears as poor application performance

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

slow container image pulls  
heavy application startup logic  
database migrations during boot  
cache warmup requirements  
large dependency initialisation

---

# First Checks

Fast checks engineers should perform.

**Examples**:

measure startup duration of new instances  
inspect image pull times  
review application boot sequence  
check readiness probe delays  
validate cache warmup behaviour

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

instance startup time metrics  
container readiness events  
serverless cold start traces  
queue backlog growth  
autoscaler response timelines

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

smaller container images  
faster startup paths  
warm pools or pre-scaling  
startup dependency optimisation  
readiness and warmup testing

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>