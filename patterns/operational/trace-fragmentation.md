# Pattern: Trace Fragmentation

## Description

Trace Fragmentation occurs when distributed traces fail to connect across services.

Instead of a complete request path, engineers see partial traces, making it difficult to understand request flow during incidents.

---

# Typical Symptoms

**Examples**:

incomplete distributed traces
missing spans between services
broken request chains
inconsistent trace IDs
trace visualisation gaps

---

# Common Misleading Signals

**Examples**:

looks like network failure
appears like service timeout
suggests instrumentation bug
seems like missing request data

---

# Likely Root Causes

**Examples**:

inconsistent trace context propagation
instrumentation mismatch between services
tracing library incompatibility
incorrect middleware configuration
sampling configuration mismatch

---

# First Checks

**Examples**:

verify trace context propagation
inspect instrumentation libraries
check trace headers between services
validate tracing configuration
inspect recent deployments

---

# Useful Signals

**Examples**:

trace spans
service request logs
distributed trace visualisations
propagation headers
tracing system metrics

---

# Prevention

**Examples**:

consistent tracing standards
shared instrumentation libraries
trace propagation validation
distributed tracing audits
observability testing

---

<a href="../../categories/operational/operational.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>