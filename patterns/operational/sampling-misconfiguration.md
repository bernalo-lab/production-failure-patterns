# Pattern: Sampling Misconfiguration

## Description

Sampling Misconfiguration occurs when observability systems sample too little or too much telemetry data.

When sampling is too aggressive, important diagnostic data may be lost. When sampling is too low, observability systems may become overloaded.

---

# Typical Symptoms

**Examples**:

missing traces during incidents
inconsistent observability data
observability pipeline overload
incomplete diagnostic data
metrics showing partial behaviour

---

# Common Misleading Signals

**Examples**:

looks like trace collection failure
appears like instrumentation bug
suggests monitoring outage
traces randomly missing

---

# Likely Root Causes

**Examples**:

incorrect trace sampling rate
dynamic sampling misconfiguration
observability system overload
deployment configuration error
tracing collector limits

---

# First Checks

**Examples**:

inspect sampling configuration
check tracing pipeline load
review recent configuration changes
verify collector throughput
inspect trace storage metrics

---

# Useful Signals

**Examples**:

trace sampling metrics
collector logs
observability pipeline throughput
instrumentation metrics
tracing system health

---

# Prevention

**Examples**:

sampling configuration review
adaptive sampling strategies
observability pipeline monitoring
telemetry load testing
tracing configuration standards

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>