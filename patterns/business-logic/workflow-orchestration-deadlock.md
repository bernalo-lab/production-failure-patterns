# Pattern: Workflow Orchestration Deadlock

## Description

**Workflow Orchestration Deadlock** happens when multiple services or workflow steps wait indefinitely for each other to complete, preventing forward progress.

This creates silent operational failures because systems appear alive but business processes stop moving.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

orders stuck in pending state  
background jobs never complete  
workflow timeout alerts  
dependent services waiting forever  
manual intervention required to unblock progress

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like queue slowdown  
appears like database issue  
seems like dependency outage  
blamed on network latency  
appears as intermittent workflow delay

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

circular service dependencies  
incorrect wait conditions  
missing timeout boundaries  
state transition bugs  
orchestrator logic flaws

---

# First Checks

Fast checks engineers should perform.

**Examples**:

trace workflow step progression  
identify blocked dependency states  
review timeout configurations  
inspect orchestration logs  
validate state transition rules

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

workflow execution traces  
state machine logs  
timeout failure events  
pending transaction dashboards  
orchestrator wait condition logs

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

explicit timeout boundaries  
deadlock detection monitoring  
clear workflow state design  
dependency graph validation  
failure path testing

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>