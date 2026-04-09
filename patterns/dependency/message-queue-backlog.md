# Pattern: Message Queue Backlog

## Description

Message Queue Backlog occurs when producers send messages faster than consumers can process them.

Over time, messages accumulate, causing delays and potential system instability.

---

## Typical Symptoms

Engineers may observe:

Queue depth growth
Message processing delays
Consumer lag
Increased latency

---

## Common Misleading Signals

The issue may appear as:

Traffic spike
Consumer crash

---

## Likely Root Causes

Typical causes include:

Slow consumer processing
Consumer failures
Traffic bursts

---

## First Checks

Engineers should check:

Queue depth metrics
Consumer health
Processing latency

---

## Useful Signals

Look for:

Queue size metrics
Consumer lag dashboards

---

## Prevention

**Autoscaling Consumers**
Increase processing capacity dynamically.

**Backpressure**
Slow producers when queues grow.

---

<a href="../../categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>