# Pattern: Autoscaler Feedback Loop Failure

## Description

**Autoscaler Feedback Loop Failure** happens when scaling systems respond too slowly, too aggressively, or based on misleading signals, causing instability instead of recovery.

Instead of stabilising the platform, scaling actions amplify the incident through oscillation, delayed recovery, or resource waste.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

services repeatedly scale up and down  
latency remains high despite scaling  
new instances fail to reduce pressure  
cost spikes during incidents  
resource exhaustion despite autoscaler activity

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like autoscaler is working correctly  
appears like traffic unpredictability  
seems like dependency bottleneck  
blamed on deployment quality  
appears as random capacity failure

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

slow scaling thresholds  
incorrect target metrics  
cold start delays  
scaling based on lagging indicators  
insufficient maximum capacity settings

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review autoscaler event history  
validate scaling trigger metrics  
check instance startup times  
inspect maximum scaling limits  
compare scaling activity with traffic spikes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

autoscaler event logs  
CPU and latency scaling graphs  
instance startup duration metrics  
resource saturation dashboards  
traffic versus capacity comparisons

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

better autoscaler tuning  
faster startup paths  
predictive scaling for known events  
safe scaling limits  
autoscaler simulation testing

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
