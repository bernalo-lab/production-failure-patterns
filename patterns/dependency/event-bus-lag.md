# Pattern: Event Bus Lag

## Description

Event Bus Lag occurs when event propagation across distributed systems slows down.

Events remain in the event stream longer than expected, delaying downstream processing.

---

## Typical Symptoms

Engineers may observe:

Consumer lag
Event processing delays
Event replay accumulation

---

## Common Misleading Signals

The issue may appear as:

Service latency
Event handler bugs

---

## Likely Root Causes

Typical causes include:

Broker overload
Slow consumers
Partition imbalance

---

## First Checks

Engineers should check:

Consumer offsets
Broker health
Event throughput

---

## Useful Signals

Look for:

Event processing lag metrics
Broker resource usage

---

## Prevention

**Partition Scaling**
Increase event partitions.

**Consumer Parallelism**
Process events faster.

---

<a href="../../categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>