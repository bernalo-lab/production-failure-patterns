# Pattern: Human Approval Bottleneck Failure

## Description

**Human Approval Bottleneck Failure** happens when manual approval steps become delayed, blocked, or unavailable, causing automated workflows to stall.

This often creates invisible operational incidents because the platform is technically healthy, but business outcomes stop progressing.

---

# Typical Symptoms

What engineers usually observe.

**Examples**:

orders stuck awaiting approval  
payment reviews delayed for hours  
release approvals blocking deployments  
customer onboarding frozen in pending state  
large backlog of unprocessed manual tasks

---

# Common Misleading Signals

Signals that often send engineers down the wrong path.

**Examples**:

looks like workflow bug  
appears like queue consumer issue  
seems like service outage  
blamed on orchestration delays  
appears as random operational slowdown

---

# Likely Root Causes

Typical reasons this pattern occurs.

**Examples**:

approver unavailable or overloaded  
approval routing misconfiguration  
missing escalation paths  
manual review spikes during incidents  
notification failures for approvers

---

# First Checks

Fast checks engineers should perform.

**Examples**:

review approval queue backlog  
validate approver assignment  
check notification delivery status  
inspect escalation triggers  
compare approval SLA trends

---

# Useful Signals

Logs, metrics, or traces that help confirm the issue.

**Examples**:

approval workflow logs  
pending review dashboards  
notification delivery failures  
manual task backlog metrics  
SLA breach reports

---

# Prevention

What can reduce the likelihood of this pattern.

**Examples**:

approval escalation policies  
backup approver assignments  
approval SLA monitoring  
notification validation  
automation for low-risk approvals

---

<a href="../../categories/business-logic/business-logic.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
