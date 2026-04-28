# Pattern: Connection Leak Saturation

## Description

**Connection Leak Saturation** happens when database, API, or service connections are opened but not properly released, gradually exhausting available connection capacity.

This causes request failures even though the downstream dependency itself may still be healthy.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

database connection errors  
increasing request latency  
services hanging during requests  
connection pool exhaustion alerts  
application restarts temporarily fixing the issue

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like database outage  
appears like network issue  
seems like dependency slowdown  
blamed on traffic spikes  
appears as random timeout behaviour

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

unclosed database sessions  
failed connection cleanup  
long-running transactions  
pool misconfiguration  
retry loops holding connections too long

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review active connection counts  
inspect connection pool saturation  
check recent code changes  
validate transaction duration  
compare connection open vs close rates

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

connection pool metrics  
database session logs  
transaction duration dashboards  
timeout traces  
application restart recovery patterns

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

connection lifecycle monitoring  
pool limits with alerts  
safe timeout defaults  
transaction duration limits  
connection leak testing

---

<a href="../../categories/capacity/capacity.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
