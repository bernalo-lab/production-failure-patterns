# Pattern: Kernel Resource Limits Reached

## Description

Kernel Resource Limits Reached occurs when operating system-level limits such as file descriptors, process limits, sockets, or threads are exhausted.

This creates sudden failures even when application metrics appear healthy because the failure occurs below the application layer.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

sudden connection failures
inability to open files
thread creation failures
application crashes
service degradation without obvious cause

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

Looks like random application bug
Appears like dependency outage
Seems like infrastructure instability
Monitoring shows healthy CPU and memory

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

file descriptor exhaustion
thread leaks
excessive open sockets
low ulimit settings
runaway processes
poor connection cleanup

---

# First Checks

Fast checks engineers should perform.

**Examples**:

open file descriptor count
process/thread counts
socket usage
ulimit configuration
recent deployment changes

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

kernel logs
file descriptor metrics
socket count metrics
thread creation errors
process limit alerts

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

sensible ulimit configuration
connection cleanup
resource monitoring
thread pool management
process leak detection

---

<a href="../../categories/Infrastructure/infrastructure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>