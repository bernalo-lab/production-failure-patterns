# Pattern: Slow Burn Capacity Exhaustion

## Description

**Slow Burn Capacity Exhaustion** happens when system resources gradually degrade over time rather than failing suddenly.

Unlike sharp incidents, this pattern slowly builds through increasing load, inefficient usage, or hidden leaks until latency rises, retries increase, and the platform eventually reaches failure thresholds.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

gradual latency increase  
steady memory growth  
CPU usage slowly rising  
queue depth increasing over hours or days  
intermittent timeout failures before major outage

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like random traffic growth  
appears like dependency instability  
seems like poor deployment quality  
blamed on isolated user behaviour  
appears as normal peak-hour variance

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

memory leaks  
connection pool exhaustion  
slow query accumulation  
unbounded retries  
inefficient background jobs

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review long-term CPU and memory trends  
check connection pool usage  
inspect queue growth patterns  
validate retry rates  
compare resource usage before and after recent changes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

memory usage graphs  
connection pool metrics  
queue depth dashboards  
retry rate metrics  
historical latency trends

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

capacity planning  
resource trend monitoring  
leak detection alerts  
retry budgets  
load testing under sustained traffic

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
